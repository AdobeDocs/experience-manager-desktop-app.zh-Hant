---
title: 開始使用 [!DNL Experience Manager] 案頭應用程式
description: 瞭解 [!DNL Experience Manager] 案頭應用程式如何透過簡化的工作流程和生產力功能，來強化內容的建立與發佈。
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '1213'
ht-degree: 0%

---


# 開始使用[!DNL Adobe Experience Manager]案頭應用程式 {#getting-started-desktop-app}

使用[!DNL Adobe Experience Manager]案頭應用程式來存取儲存在本機案頭上[!DNL Adobe Experience Manager] DAM存放庫中的數位資產。 然後您就可以在任何案頭應用程式中使用這些資產。 您可以在案頭應用程式中在本機開啟及編輯資產。 進行變更後，請透過版本控制將它們上傳回[!DNL Experience Manager]以與其他使用者共用更新。 您也可以將新檔案和資料夾階層上傳到[!DNL Experience Manager]、建立資料夾，以及從[!DNL Experience Manager] DAM中刪除資產或資料夾。

整合可讓組織中的不同角色集中管理[!DNL Experience Manager Assets]中的資產，並在Windows或macOS上的原生應用程式中存取本機案頭上的資產。

當您在登出後或第一次開啟應用程式時，請以[!DNL Experience Manager]格式提供您`https://[aem-server-url]:[port]/`伺服器的URL。 然後選取[!UICONTROL Connect]選項。 提供認證以將應用程式連線至伺服器。

您使用[!DNL Adobe Experience Manager]案頭應用程式執行的主要工作為：

![您可以使用[!DNL Experience Manager]案頭應用程式完成的工作流程與工作](assets/aem_desktop_app_usecases_v2.png)

## 案頭應用程式的運作方式 {#how-app-works2}

開始使用應用程式之前，請先瞭解[應用程式的運作方式](release-notes.md#how-app-works)。 此外，請熟悉下列詞語：

* **[!UICONTROL Desktop Actions]**：從Assets Web介面中，在瀏覽器內可探索資產位置或取出並開啟資產，以在原生案頭應用程式中編輯。 這些動作可從Web介面取得，並使用案頭應用程式功能。

* 檔案狀態為&#x200B;**[!UICONTROL Cloud Only]**：這類資產未在本機電腦上下載，僅可在[!DNL Experience Manager]伺服器上使用。

* 檔案狀態為&#x200B;**[!UICONTROL Available locally]**：資產已下載，並可在本機電腦上使用。 資產不會變更。

* 檔案狀態為&#x200B;**[!UICONTROL Edited locally]**：此類資產已在本機修改，且變更仍會保留至已上傳至[!DNL Experience Manager]伺服器的檔案。 上傳之後，狀態會變更為[!UICONTROL Available locally]。 請參閱[編輯資產](upload-assets.md#edit-assets-upload-updated-assets)。

* 檔案狀態為&#x200B;**[!UICONTROL Editing conflict]**：如果您與其他人同時編輯資產，應用程式會指出發生編輯衝突。 應用程式也提供保留或捨棄變更的選項。 請參閱[如何避免編輯衝突](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts)。

* 檔案狀態為&#x200B;**[!UICONTROL Modified remotely]**：應用程式會指出您已下載的資產是否已在[!DNL Experience Manager]伺服器上變更。 應用程式也提供下載最新版本和更新本機復本的選項。 請參閱[如何避免編輯衝突](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts)。

* **[!UICONTROL Check-out]**：如果您正在編輯檔案或要編輯檔案，請切換狀態以簽出。 它會在應用程式和[!DNL Experience Manager]網頁介面的資產上新增鎖定圖示。 鎖定圖示會向其他使用者指示，以避免同時編輯相同的資產，因為這會導致編輯衝突。

* **[!UICONTROL Check-in]**：將資產標示為可供其他使用者編輯，而不會造成編輯衝突。 上傳變更時，鎖定圖示會自動移除。 切換籤入狀態也會移除鎖定圖示，不過Adobe建議您避免手動簽入而不上傳變更。 如果您捨棄變更，請手動切換入庫。

* **[!UICONTROL Open]**&#x200B;動作：只要開啟資產，即可在原生應用程式中預覽。 Adobe建議您避免使用此動作來編輯資產。 原因是它不會簽出資產。 同時，其他使用者也可以進行編輯，導致編輯衝突。

* **[!UICONTROL Edit]**&#x200B;動作：使用動作來修改影像。 按一下[!UICONTROL Edit]取出資產並在資產上新增鎖定圖示。 按一下「編輯」後，如果您不想編輯資產，請按一下[!UICONTROL Toggle check-in]。 若要刪除、重新命名或移動[!DNL Experience Manager] DAM資料夾階層中的資產，請使用[!DNL Experience Manager] Web介面動作，而非編輯動作。

* **[!UICONTROL Download]**&#x200B;動作：將資產下載到您的本機電腦。 您現在可以下載資產，稍後再進行編輯；離線工作稍後再上傳變更。 Assets會下載到檔案系統的快取資料夾中。

* **[!UICONTROL Reveal File]**&#x200B;或&#x200B;**[!UICONTROL Reveal Folder]**&#x200B;動作：將資產下載至本機快取資料夾時，應用程式會模擬本機網路磁碟機。 它提供每個資產的本機路徑。 若要知道此路徑，請使用應用程式中適當的顯示選項。 需要顯示動作才能在Creative Cloud應用程式中放置資產。 請參閱[置入資產](search.md#place-assets-in-native-documents)。

* **[!UICONTROL Open In Web]**&#x200B;動作：若要在[!DNL Experience Manager]網頁介面中檢視資產，請在網頁中開啟該資產。 您可以從[!DNL Experience Manager]介面啟動更多工作流程，例如更新中繼資料或資產探索。

* **[!UICONTROL Delete]**&#x200B;動作：從[!DNL Experience Manager] DAM存放庫中刪除資產。 該動作會刪除Experience Manager伺服器上的資產原始副本。 如果您只想捨棄本機資產的修改，請參閱[捨棄變更](upload-assets.md#edit-assets-upload-updated-assets)。

* **[!UICONTROL Upload Changes]**：案頭應用程式只有在您明確上傳至[!DNL Experience Manager]伺服器時，才會上傳更新的資產。 當您儲存編輯時，變更只會儲存在本機電腦上。 上傳時，資產會自動入庫，且鎖圖示會移除。 請參閱[編輯資產](upload-assets.md#edit-assets-upload-updated-assets)。

## 在[!DNL Experience Manager]網頁介面中啟用案頭動作 {#desktopactions-v2}

從瀏覽器的[!DNL Assets]使用者介面中，您可以探索資產位置或取出並開啟資產，以在您的案頭應用程式中進行編輯。 這些選項稱為[!UICONTROL Desktop Actions]，預設不會啟用。 若要啟用此功能，請依照下列步驟執行。

1. 在[!DNL Assets]主控台中，按一下工具列中的&#x200B;**[!UICONTROL User]**&#x200B;圖示。
1. 按一下&#x200B;**[!UICONTROL My Preferences]**&#x200B;以顯示&#x200B;**[!UICONTROL Preferences]**&#x200B;對話方塊。

1. 在[!UICONTROL User Preferences]對話方塊中，選取&#x200B;**[!UICONTROL Show Desktop Actions For Assets]**，然後按一下&#x200B;**[!UICONTROL Accept]**。

   ![選取[顯示Assets的案頭動作]以啟用案頭動作](assets/enable_desktop_actions1.png)

## 從[!DNL Assets] Web介面開始 {#adv-workflow-start-from-aem-ui}

如有需要，請從Assets網頁介面啟動您的工作流程。 案頭應用程式會與[!DNL Experience Manager]整合，以便在使用「案頭動作」提出要求時接管。

從Web介面啟動工作流程的一個特殊情況是資產探索。 Assets使用者介面中的Omnisearch列提供豐富而進階的搜尋體驗。 您可能想要先在網頁上找到想要的資產，然後使用[!UICONTROL Desktop Actions]在應用程式中啟動工作流程。 某些範例案例包含使用Facet篩選搜尋結果、尋找從Adobe Stock授權的特定資產，或貴組織實作的自訂，以便您更妥善地從Web介面探索。

當您嘗試在Assets網頁介面上執行下列動作時，就會使用案頭應用程式功能：

* 允許[!UICONTROL Desktop Actions]、[!UICONTROL Open]和[!UICONTROL Edit]的[!UICONTROL Reveal]
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] 或 [!UICONTROL check-in]

例如，Web介面上可用於應用程式中取出之資產的動作是[!UICONTROL Open]、[!UICONTROL Reveal]和[!UICONTROL Check in]。

![在[!DNL Experience Manager]網頁介面中的案頭動作](assets/assets_web_actions_da2.png "在Experience Manager網頁介面中的案頭動作")

>[!NOTE]
>
>瀏覽器可能會提示您允許啟動[!DNL Adobe Experience Manager]案頭。 若要每次都能不間斷地從瀏覽器傳輸至應用程式，請選取適當的核取方塊，讓應用程式接管。

使用Web介面找不到下列資訊或工作流程。 使用案頭應用程式，因為Web介面不會追蹤本機變更，且不瞭解下列內容：

* 檔案是在本機編輯的。
* 具有編輯衝突及解決衝突方法的檔案。
* 將本機變更上傳到[!DNL Experience Manager]。
* 本機可用檔案的各種狀態。

相反地，您可以使用&#x200B;**[!UICONTROL Open In Web]**&#x200B;動作，從案頭應用程式開始在Web介面中開啟資產。

## 後續步驟 {#next-steps}

* [觀看開始使用Adobe Experience Manager案頭應用程式的影片](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* 使用右側邊欄提供的[!UICONTROL Edit this page] ![編輯頁面](assets/do-not-localize/edit-page.png)或[!UICONTROL Log an issue] ![建立GitHub問題](assets/do-not-localize/github-issue.png)來提供檔案意見回饋

* 聯絡[客戶服務](https://experienceleague.adobe.com/zh-hant?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [瞭解使用者介面](/help/using/user-interface.md)
>* [發行說明和已知問題](/help/using/release-notes.md)
>* [安裝或升級案頭應用程式](/help/using/install-upgrade.md)
