---
title: 案頭應用程式v1.10最佳作法
description: 主要功能及建議使用 [!DNL Adobe Experience Manager] 案頭應用程式1.10版。
exl-id: 5de06b33-c05c-47eb-b884-408b6f9afc94
source-git-commit: 1c7437786a50eeafa884ce92b745f3438b2d2b88
workflow-type: tm+mt
source-wordcount: '1651'
ht-degree: 0%

---

# AEM案頭應用程式v1.10最佳作法 {#aem-desktop-app-best-practices}

## 概觀 {#overview}

[!DNL Adobe Experience Manager]案頭應用程式會將您的數位資產管理(DAM)解決方案連結至案頭，讓您直接在案頭上開啟AEM Web UI中可用的檔案。 如果您從案頭儲存資產，資產會上傳至適當位置的AEM。

AEM案頭應用程式可讓您避免在AEM中更新不正確的本機復本或更新錯誤資產。 透過案頭作業系統提供的網路共用技術，可啟用案頭應用程式易於使用的工作流程。

案頭應用程式會將AEM Assets存放庫以網路共用形式掛載在案頭上。 因此，資料夾和檔案看起來就好像是本機資料夾和檔案。 但是，不建議直接從Finder或Explorer中掛載之網路共用中的案頭執行數位資產管理作業。 Adobe建議您改用AEM Assets網頁UI來執行操作，例如複製或移動大量資產。

>[!NOTE]
>
>閱讀本檔案之前，您可以檢閱整體[AEM和Creative Cloud整合最佳實務](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/aem-cc-integration-best-practices)，以取得主題的更高層級概觀。

## AEM案頭應用程式架構 {#aem-desktop-app-architecture}

AEM案頭應用程式使用WebDAV (Windows)或SMB (Mac)網路共用來掛載網路共用。 掛載的網路共用僅是本機的。 AEM案頭應用程式會攔截呼叫（開啟、讀取、寫入）並提供額外的本機快取。 它會將AEM Assets伺服器的遠端呼叫轉譯為最佳化的AEM HTTP請求。 下圖說明AEM案頭應用程式架構。

![AEM案頭應用程式架構](assets/arch_v1.png)

*圖：案頭應用程式架構*

儲存檔案時，寫入時額外的快取可確保檔案會先儲存在本機，讓使用者避免等待網路傳輸。 接著，在預先定義的延遲（30秒）後，檔案會在背景上傳至AEM，然後資產會上傳至AEM。 AEM案頭應用程式提供可監控背景檔案上傳狀態的UI。

## 建議使用AEM案頭應用程式 {#recommended-use-of-aem-desktop-app}

AEM案頭應用程式的主要功能包括：

* **正在從案頭上的AEM Assets Web UI開啟檔案**。 在Web UI中，您可以顯示案頭上的資產（在Finder、Explorer中），或使用案頭應用程式開啟資產。

* **取出並簽入**。 Assets可以出庫進行編輯，但在AEM Assets中會標籤為已為使用者鎖定。 編輯後，可簽入資產以將其解鎖。

* **儲存檔案的變更**。 您在網路共用中儲存至檔案的任何變更都會自動上傳至AEM，並建立一個新版本。

* **將連結的資產放入其他檔案**。 在Creative Cloud（[!DNL Adobe Photoshop]、[!DNL Adobe InDesign]和[!DNL Adobe Illustrator]）等應用程式中，您可以將外部檔案設為連結。 例如，您可以將影像置入InDesign檔案中。 在此情況下，網路共用掛載可讓您瀏覽並從AEM選取要放置的資產。 在某些非Adobe應用程式(例如MS® Office)中，也可以放置連結的檔案。

* 在AEM **中**&#x200B;參考解析度。 如果置入的檔案和含有連結的主要檔案都儲存在AEM中，它會自動提供有關資產參考的伺服器端資訊。

* **從案頭存取資產**。 在掛接的網路共用中，內容功能表會提供[!UICONTROL More Info]對話方塊（較大的預覽、關鍵中繼資料）以及在AEM UI中開啟資產的功能。

* **正在大量上傳大型階層資料夾**。 如果您在AEM使用者介面中使用&#x200B;**建立** > **資料夾上傳**&#x200B;選項來上傳資產，AEM案頭應用程式會在背景將選取的資料夾階層上傳到AEM。 使用案頭應用程式中的專用UI監控上傳進度。

## 不適當使用AEM案頭應用程式 {#inappropriate-use-of-aem-desktop-app}

* 請勿使用AEM案頭應用程式從案頭管理資產。 AEM案頭應用程式並未建置為網路磁碟機的替代專案。 請改用下列功能：

   * 適用於數位資產管理（尋找或共用資產、中繼資料，以及複製或移動）的AEM Assets Web UI。

   * AEM案頭應用程式[!UICONTROL Folder Upload]以上傳大型階層資料夾。

* 請勿將AEM案頭應用程式視為AEM Assets的「案頭同步」使用者端。 在此，AEM案頭應用程式的主要優點在於它提供「虛擬」存取整個存放庫，而案頭同步應用程式通常只同步屬於一個使用者的資產。 AEM案頭應用程式提供某種程度的快取和背景上傳；不過，它的運作方式與典型「同步」應用程式非常不同，例如Adobe Creative Cloud案頭應用程式或Microsoft OneDrive。

* 請勿經常使用AEM案頭應用程式網路磁碟機來儲存資產。 所有儲存操作都會傳輸至AEM Assets。 因此，直接在掛接的AEM Assets存放庫中執行大量編輯作業是不切實際的。 直接在掛接的存放庫中編輯資產時，會使用不相關的版本卡住資產的時間軸，並在伺服器上施加額外的經常性費用。

* 請勿使用AEM案頭應用程式將大量資料從一個AEM執行個體移轉至另一個執行個體。 請參閱[移轉指南](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/assets-migration-guide)以規劃及執行資產移轉。 相反地，案頭應用程式[在[!DNL Adobe Experience Manager]中首次支援大量上傳](use-app-v1.md#bulkupload)大量資產。

## 適用於選定使用案例的Recommendations {#recommendations-for-selected-use-cases}

### 創意使用者的資產存取權 {#access-to-assets-for-creative-users}

AEM案頭應用程式可提供整個DAM存放庫的虛擬存取，而案頭上的創意使用者要在他們的案頭上尋找和存取正確的資產可能會相當複雜。 使用這些最佳實務來簡化流程。

* 使用AEM Assets Web UI中的共同作業功能，讓創意使用者更直接地存取正確的資產。 共用資料夾或集合、提供智慧型集合（已儲存的搜尋）或傳送包含正確資產指標的通知，只是其中的一部分。 創意使用者可以在Web UI中使用案頭動作，以快速存取其案頭上的這些資產。

* 考慮資產（存取控制）的正確許可權，以簡化創意使用者在DAM存放庫中的檢視，基本上是限制他們僅存取所需或感興趣的資產：

   * 某些與創意使用者無關的區域，其使用者群組可能會被拒絕，以便從他們的檢視中移除這些群組，這些檢視也在案頭上。

   * DAM中的大部分資產為最終資產，且不可用於變更，創意使用者應以唯讀方式存取這些資產。

   * 只有需要變更或修飾的資產才應為創意使用者啟用寫入功能。 有些組織會使用「AEM專案」及其建立的資料夾來託管仍會遭到變更的資產。

### 搜尋資產 {#searching-assets}

搜尋您要在案頭上開啟的檔案：

* 使用AEM Assets Web UI來找出資產。 AEM Assets中的搜尋不僅功能強大（搜尋Facet、已儲存的搜尋），還提供尋找合適資產的額外功能。 這些篩選器包括額外的篩選器，如根據狀態（核准、到期）、集合、任務、通知搜尋資產的能力，以及與其他使用者/群組共用資料夾/集合。

* 找到資產後，請在AEM UI中使用案頭動作來存取案頭上的資產。

### 更新使用AEM案頭應用程式開啟的資產 {#updating-assets-opened-using-aem-desktop-app}

如果您直接在從AEM Assets對應至本機網路共用的位置編輯資產，每次將資產儲存在案頭上時，都會將其上傳至AEM。 此外，AEM會建立版本並產生轉譯。

如果儲存在AEM中的資產需要更新：

* 針對&#x200B;**次要更新**，例如核准程式中的次要潤飾請求：

   * 取出檔案，然後在案頭上開啟。

   * 更新檔案。

   * 儲存更新的版本。 資產會更新，而時間軸會顯示原始版本以進行比較。

* 對於&#x200B;**重大更新**，例如需要小型創意WIP週期的變更請求：

   * 使用「顯示」選項，在案頭上開啟適當的資料夾。

   * 將檔案複製到對應AEM Assets共用之外的WIP資料夾(例如，將檔案複製到與Adobe Creative Cloud案頭應用程式同步的資料夾)。

   * 處理檔案並間歇儲存。 變更不會儲存至AEM Assets。

   * 編輯完成後，移動、複製或儲存從AEM對映的檔案，以將其上傳為新版本。

## 網路效能 {#network-performance}

AEM案頭應用程式的良好使用者體驗仰賴穩定的網路連線和調校良好的伺服器，尤其是在上傳和更新資產方面。 這些建議適用於組織中的網路/IT團隊。

### 網路考量事項 {#network-considerations}

若要瞭解AEM Assets網路組態的最佳實務，請前往[如何大量移轉資產](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/assets-migration-guide)檔案。 協助使用者最佳化AEM案頭應用程式體驗的一些重要方面包括：

* **使用正確設定的Dispatcher**。 使用AEM Dispatcher以獲得額外的安全性，並確保它已設定為可在Dispatcher[&#128279;](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher)後與AEM進行AEM案頭應用程式連線

* **儲存頻寬**。 使用Finder瀏覽已裝載的存放庫時，請考慮關閉Mac上Finder中的圖示預覽。 搜尋器會要求每個檔案產生預覽，並讓案頭應用程式下載資產並在本機快取。 在節省頻寬的同時，也會減少桌上型電腦使用者的使用者體驗，因此在使用大型資產或頻寬受限的存放庫時，就應該這麼做。

>[!NOTE]
>
>若要關閉圖示預覽，請在Finder中移至[!UICONTROL View]，選取[!UICONTROL View Options]，然後取消勾選[!UICONTROL Show icon preview]選項。 這僅適用於目前的資料夾 — 若要將其設為預設值，請按一下相同對話方塊中的[!UICONTROL Use as default]選項。

### 最佳化伺服器效能 {#optimizing-server-performance}

若要瞭解AEM Assets伺服器應該如何最佳化效能，請前往[AEM Assets效能調整指南](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/performance-tuning-guidelines)。 AEM案頭應用程式伺服器效能的一些重要方面與最佳化工作流程設定有關，使其可正確執行資產上傳：

* **更多效能的資產上傳**。 將[AEM資產更新工作流程模型設定為暫時性](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/performance-tuning-guidelines)。

* **限制上載的伺服器CPU**。 請確定最大平行工作流程作業引數已正確設定，這樣上傳就不會耗盡所有的CPU。
