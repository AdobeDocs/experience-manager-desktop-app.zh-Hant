---
title: 使用 [!DNL Experience Manager] 案頭應用程式下載資產
description: 使用 [!DNL Adobe Experience Manager] 案頭應用程式下載資產。
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 1%

---


# 在本機下載資產 {#download-assets-locally}

應用程式經常從[!DNL Experience Manager]伺服器下載資產到您的本機檔案系統。 下載耗用頻寬和磁碟空間。 瞭解情況有助於您最佳化完成下載的等待時間。 您可以下載本機檔案系統上的資產。 應用程式會從[!DNL Experience Manager]伺服器擷取資產，並將相同的復本儲存在本機檔案系統上。

按一下&#x200B;**[!UICONTROL More actions]** ![更多選項圖示](assets/do-not-localize/more2_da2.png)取得選項，然後按一下![下載圖示](assets/do-not-localize/download_cloud_da2.png)進行下載。

![資產下載選項](assets/download_option_da2.png "資產下載選項")

>[!NOTE]
>
>下載或上傳大型檔案或多個檔案時，應用程式會關閉對資產和資料夾的動作。 下載或上傳完成時，這些動作即可使用。

當您使用[!UICONTROL Open]動作在原生案頭應用程式中開啟資產時，如果資產尚未在本機提供，則會下載到本機。 請參閱[開啟資產](#openondesktop-v2)。

當您從應用程式內顯示資產或資料夾的位置時，資產或資料夾會先在本機下載，然後在您電腦上的本機網路共用中開啟。 請參閱[開啟資產](#openondesktop-v2)。

當您使用[!UICONTROL Edit]動作編輯原生案頭應用程式中的資產時，如果資產尚未在本機提供，則會下載到本機。 檢視[編輯資產並將更新的資產上傳到 [!DNL Experience Manager]](#edit-assets-upload-updated-assets)。

如果應用程式已安裝並獲准使用，它會在您從[!UICONTROL Desktop Actions]網頁介面使用[!DNL Experience Manager]時完成動作。 應用程式會先下載資產，然後完成動作。

## 下載多個資產 {#download-multiple-assets}

如果佇列大小很大或您遇到一些網路問題，下載多個資產可能會導致效能不佳。 此外，當您下載資料夾時，可能會無意中將許多資產排入下載佇列。 為避免冗長的等候時間，應用程式會限制單次下載的資產數量。 若要瞭解如何進行設定，請參閱[設定偏好設定](install-upgrade.md#set-preferences)。 即使低於此限制，應用程式有時也可能會在下載明顯大型的資料夾之前尋求確認。

![應用程式確認下載相對大量資產](assets/download_confirmation_da2.png "應用程式確認下載相對大量資產")

如果選取並下載資料夾，應用程式只會下載直接儲存在[!DNL Experience Manager]中資料夾中的資產。 它不會自動從子資料夾中下載資產。

## 後續步驟 {#next-steps}

* [觀看開始使用Adobe Experience Manager案頭應用程式的影片](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* 使用右側邊欄提供的[!UICONTROL Edit this page] ![編輯頁面](assets/do-not-localize/edit-page.png)或[!UICONTROL Log an issue] ![建立GitHub問題](assets/do-not-localize/github-issue.png)來提供檔案意見回饋

* 聯絡[客戶服務](https://experienceleague.adobe.com/zh-hant?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [上傳資產](/help/using/upload-assets.md)
>* [瞭解使用者介面](/help/using/user-interface.md)
>* [搜尋](/help/using/search.md)

