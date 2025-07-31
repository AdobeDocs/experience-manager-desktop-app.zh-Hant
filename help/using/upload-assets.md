---
title: 使用 [!DNL Experience Manager] 案頭應用程式上傳資產
description: 使用 [!DNL Adobe Experience Manager] 案頭應用程式上傳資產。
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 1%

---


# 上傳資產 {#upload-assets}

## 編輯資產並將更新的資產上傳到[!DNL Experience Manager] {#edit-assets-upload-updated-assets}

當您想要進行變更並將更新的資產上傳到[!DNL Experience Manager]伺服器時，請開啟要編輯的資產。 為避免與其他使用者的編輯發生衝突，請使用應用程式來起始編輯工作階段。 開始編輯之前，請確定資產上沒有鎖定圖示，表示有其他使用者正在編輯資產。

若要編輯資產，請搜尋資產或瀏覽至資產位置。 按一下![其他圖示](assets/do-not-localize/more2_da2.png)並按一下&#x200B;**[!UICONTROL Edit]**。

使用&#x200B;**[!UICONTROL Toggle Check-out]**&#x200B;鎖定資產，以防止在下列兩種情況下與其他使用者的編輯發生衝突：

* 您已開始編輯資產，但未先將資產出庫（例如，直接開啟資產）。
* 您打算儘快開始編輯資產，不希望其他人編輯。

完成編輯後，應用程式會顯示已變更資產的&#x200B;**[!UICONTROL Edited Locally]**&#x200B;狀態。 儲存至資產的所有變更僅在本機進行，直到您將變更上傳至[!DNL Experience Manager]為止。 若要逐一上傳個別或數個資產，請從資產的選項中按一下&#x200B;**[!UICONTROL Upload Changes]**。 它會在[!DNL Experience Manager]中建立資產的版本。 使用[!DNL Assets]的Web介面，您可以在[時間軸檢視](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/using/activity-stream)中看到資產歷史記錄。

![在應用程式中上傳變更選項](assets/upload_changes_single1_da2.png "在應用程式中上傳變更選項")

![檢視大型資產預覽時上傳變更選項](assets/upload_changes_single2_da2.png "檢視大型資產預覽時上傳變更選項")

如需有關協同編輯的最佳實務，請參閱[進階工作流程：在相同的檔案上共同作業並避免編輯衝突](#adv-workflow-collaborate-avoid-conflicts)。

在下列情況下，您可能會想要捨棄本機資產的變更和編輯。 按一下「**[!UICONTROL Discard Changes]**」。

* 如果您不想將變更儲存在[!DNL Experience Manager]本機。
* 儲存部分變更後，開始變更原始資產。
* 停止編輯不再需要的資產。

如有必要，請切換出庫。 更新的資產會從本機快取資料夾中移除，並在您編輯或開啟時再次下載。

## 上傳新資產到[!DNL Experience Manager] {#upload-and-add-new-assets-to-aem}

使用者可新增資產至DAM存放庫。 例如，您可能是想要從拍照新增大量像片至[!DNL Experience Manager]存放庫的代理攝影師或承包商。 若要新增內容至[!DNL Experience Manager]，請選取應用程式頂端列中的![上傳至雲端選項](assets/do-not-localize/upload_to_cloud_da2.png)。 瀏覽至本機檔案系統中的資產檔案，然後按一下&#x200B;**[!UICONTROL Select]**。 或者，若要上傳資產，請在應用程式介面上拖曳檔案或資料夾。 在Windows上，如果您在應用程式內的資料夾中拖曳資產，資產會上傳至資料夾。 如果上傳時間較長，應用程式會顯示進度列。

<!-- ![Download progress bar for large-sized assets](assets/upload_status_da2.png "Download progress bar for large-sized assets")
-->

您可以從您的本機檔案系統上傳資料夾或個別檔案。 資料夾的階層會在上傳時保留。 大量上傳資產之前，請參閱[大量上傳](#bulk-upload-assets)。

若要檢視指定工作階段中傳輸的資產清單，請按一下「**[!UICONTROL View]** > **[!UICONTROL Assets transfers]**」。 清單可讓您檢視並快速驗證目前工作階段的檔案傳輸。

![特定工作階段中的已轉移資產清單](assets/assets_transfered_da2.png "特定工作階段中的已轉移資產清單")

您可以在&#x200B;**[!UICONTROL Preferences]** > **[!UICONTROL Upload acceleration]**&#x200B;設定中控制上傳並行（加速）。 更多並行作業通常可讓上傳速度更快，但可能會耗費大量資源，耗用本機電腦的更多處理能力。 如果系統速度緩慢，請使用較低的並行值來重新嘗試上傳。

>[!NOTE]
>
>傳輸清單不是永久性的，而且如果您結束應用程式並重新開啟應用程式，將無法使用。

## 大量上傳資產 {#bulk-upload-assets}

使用者或組織（例如攝影師或創意代理商）可在拍攝、潤飾或從較大集合中選取等活動中建立許多本機資產。 這些工作通常在[!DNL Experience Manager]之外完成。 他們可以直接從案頭應用程式上傳這些大型本機資料夾到[!DNL Assets]。 會保留資料夾階層，並上傳所有巢狀子資料夾和包含的資產。 相同伺服器的其他使用者也可以立即使用上傳的資產。 Assets會在背景上傳，因此操作不會繫結至網頁瀏覽器工作階段。

![從您的案頭大量上傳多個本機資料夾到[!DNL Experience Manager]](assets/upload_local_folders_da2.png "從您的案頭大量上傳多個本機資料夾到Experience Manager")

上傳後，如果預期變更未反映在應用程式中，請按一下重新整理圖示![重新整理圖示](assets/do-not-localize/refresh.png)。

>[!NOTE]
>
>請勿使用上傳功能跨兩個[!DNL Experience Manager]部署移轉資產。 請參閱[移轉指南](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/assets-migration-guide)。

## 後續步驟 {#next-steps}

* [觀看開始使用Adobe Experience Manager案頭應用程式的影片](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* 使用右側邊欄提供的[!UICONTROL Edit this page] ![編輯頁面](assets/do-not-localize/edit-page.png)或[!UICONTROL Log an issue] ![建立GitHub問題](assets/do-not-localize/github-issue.png)來提供檔案意見回饋

* 聯絡[客戶服務](https://experienceleague.adobe.com/?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [下載資產](/help/using/download-assets.md)
>* [瞭解使用者介面](/help/using/user-interface.md)
>* [搜尋](/help/using/search.md)
