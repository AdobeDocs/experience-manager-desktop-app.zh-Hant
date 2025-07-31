---
title: 在[!DNL Experience Manager]案頭應用程式中瀏覽、搜尋及預覽資產
description: 在 [!DNL Adobe Experience Manager] 案頭應用程式中瀏覽、搜尋及預覽資產。
feature: Desktop App
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---


# 瀏覽、搜尋和預覽資產 {#browse-search-preview-assets}

您可以瀏覽至、搜尋及預覽[!DNL Experience Manager]存放庫中的可用資產，所有這一切都是從案頭應用程式中進行。 在應用程式中嘗試下列操作：

1. 瀏覽至資料夾，並檢視資料夾中可用資產的一些基本資訊，以及所有資產的小縮圖。

   ![瀏覽DAM檔案和資料夾](assets/browse_folder_da2.png "瀏覽DAM檔案和資料夾")

1. 若要檢視詳細資訊和個別資產的大型縮圖，請按一下檔案名稱。

   ![檢視資產和動作的大型預覽](assets/large_preview_actions_da2.png "檢視資產和動作的大型預覽")

1. 按一下&#x200B;**[!UICONTROL Open]**&#x200B;或&#x200B;**[!UICONTROL Edit]**&#x200B;將檔案下載到本機，然後分別檢視檔案或在原生應用程式中進行編輯。
1. 使用關鍵字搜尋，以在[!DNL Experience Manager]存放庫中尋找相關資產。 使用`?`和`*`做為萬用字元。 這些萬用字元會分別取代單一字元或多個字元。 依需要篩選及排序結果。

   ![使用星號萬用字元的範例搜尋](assets/search_wildcard_da2.png "使用星號萬用字元的範例搜尋")

   ![另一個使用星號萬用字元的範例搜尋](assets/search_wildcard2_da2.png "另一個星號萬用字元位置不同的範例搜尋")

>[!NOTE]
>
>應用程式會透過符合多個中繼資料欄位的搜尋條件來顯示資產，而不只是資產的標題或檔案名稱。

## 在案頭上開啟資產 {#openondesktop-v2}

您可以開啟遠端資產，以便在原生應用程式中檢視。 資產會下載至本機資料夾。 然後，它們會在與檔案格式相關的原生應用程式中啟動。 您可以變更原生應用程式，以在Mac或Windows中開啟特定檔案型別（副檔名）。

按一下資產功能表中的&#x200B;**[!UICONTROL Open]**。 資產會從本機下載，並以原生應用程式開啟。 檢查狀態列中大型資產的下載進度和傳輸速度。

<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")
-->

>[!NOTE]
>
>如果預期變更未反映在應用程式中，請按一下重新整理圖示![重新整理圖示](assets/do-not-localize/refresh.png)，或在應用程式介面中按一下滑鼠右鍵，然後按一下&#x200B;**[!UICONTROL Refresh]**。 進行較大型的下載或上傳時，無法使用這些動作。

若要開啟資產的本機下載資料夾，請按一下![更多動作圖示](assets/do-not-localize/more2_da2.png)，然後按一下![顯示圖示](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]**&#x200B;動作。

## 使用資產或將資產放入原生檔案 {#place-assets-in-native-documents}

在某些情況下，例如將資產放入原生檔案時，您可以在Windows檔案總管或Mac Finder中存取檔案。 若要移至本機下載檔案的檔案系統位置，請使用![顯示圖示](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]**&#x200B;選項。

![顯示資產的檔案動作](assets/revealfile_action_da2.png "顯示資產的檔案動作")

按一下資料夾上的&#x200B;**[!UICONTROL Reveal File]**&#x200B;或&#x200B;**[!UICONTROL Reveal Folder]**，以使用本機電腦上預先選取的檔案或資料夾開啟Windows檔案總管或Mac Finder。 例如，在支援放置或連結本機檔案的原生應用程式中放置[!DNL Experience Manager]檔案時，選項很有用。 若要瞭解如何在Adobe InDesign中放置檔案，請參閱[放置圖形](https://helpx.adobe.com/indesign/using/placing-graphics.html)。

**[!UICONTROL Reveal File]**&#x200B;動作會開啟本機網路共用。 它只會顯示本機可用的資產。 也就是說，會顯示使用應用程式揭露、下載或開啟/編輯的資產。 本機網路共用沒有上傳任何變更到[!DNL Experience Manager]。 若要上傳變更，請明確使用應用程式中的&#x200B;**[!UICONTROL Upload Changes]**&#x200B;或&#x200B;**[!UICONTROL Upload]**&#x200B;動作。

>[!NOTE]
>
>為了與[!DNL Experience Manager]案頭應用程式v1.x回溯相容，顯示的檔案是從本機網路共用提供，只會公開本機可用的檔案。 顯示檔案的案頭路徑與應用程式v1.x建立的路徑相同。

>[!CAUTION]
>
>請勿使用&#x200B;**[!UICONTROL Reveal File]**&#x200B;選項編輯原生應用程式中的資產。 請改用&#x200B;**[!UICONTROL Edit]**&#x200B;動作。 若要瞭解更多資訊，請參閱[進階工作流程：共同作業相同的檔案，避免編輯衝突](#adv-workflow-collaborate-avoid-conflicts)。

### 管理資產名稱中的特殊字元 {#special-characters-in-filename}

在舊版應用程式中，在存放庫中建立的節點名稱會保留使用者提供的資料夾名稱空格和大小寫。 若要讓目前應用程式模擬v1.10應用程式的節點命名規則，請在[!UICONTROL Use legacy conventions when creating nodes for assets and folders]中啟用[!UICONTROL Preferences]。 檢視[應用程式偏好設定](/help/using/install-upgrade.md#set-preferences)。 此舊版偏好設定預設為停用。

>[!NOTE]
>
>應用程式只會使用下列命名慣例變更存放庫中的節點名稱。 應用程式會保留資產的`Title`不變。

| 字元‡ | 應用程式中的舊版偏好設定 | 當出現在檔案名稱中 | 當出現在資料夾名稱中時 | 範例 |
|---|---|---|---|---|
| `. / : [ ] \| *` | 啟用或停用 | 已取代為`-` （連字型大小）。 副檔名中的`.` （點）會維持原狀。 | 已取代為`-` （連字型大小）。 | `myimage.jpg`保持原狀，且`my.image.jpg`變更為`my-image.jpg`。 |
| `% ; # , + ? ^ { } "`和空格 | ![取消選取圖示](assets/do-not-localize/deselect-icon.png)已停用 | 保留空格 | 已取代為`-` （連字型大小）。 | `My Folder.`變更為`my-folder-`。 |
| `# % { } ? & .` | ![取消選取圖示](assets/do-not-localize/deselect-icon.png)已停用 | 已取代為`-` （連字型大小）。 | 不適用 | `#My New File.`變更為`-My New File-`。 |
| 大寫字 | ![取消選取圖示](assets/do-not-localize/deselect-icon.png)已停用 | 大小寫維持原狀。 | 變更為小寫字元。 | `My New Folder`變更為`my-new-folder`。 |
| 大寫字 | ![選取專案核取圖示](assets/do-not-localize/selection-checked-icon.png)已啟用 | 大小寫維持原狀。 | 大小寫維持原狀。 | 不適用 |

‡字元清單是以空格分隔的清單。

## 尋找所有已編輯的影像 {#find-all-edited-images}

應用程式會提供一個名為&#x200B;**[!UICONTROL Edited locally]**&#x200B;的檢視，讓您快速存取所有您在本機下載的檔案（透過[!UICONTROL Open]或[!UICONTROL Edit]動作），然後再修改。 應用程式可讓您選取所有在本機編輯的資產，並按幾下滑鼠即可上傳變更。 此檢視也會顯示有編輯衝突的本機編輯資產。

![篩選以檢視所有本機編輯的資產](assets/edited_locally_filter_da2.png "例如，篩選以檢視所有本機編輯的資產以進行大量編輯上傳")

## 後續步驟 {#next-steps}

* [觀看開始使用Adobe Experience Manager案頭應用程式的影片](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* 使用右側邊欄提供的[!UICONTROL Edit this page] ![編輯頁面](assets/do-not-localize/edit-page.png)或[!UICONTROL Log an issue] ![建立GitHub問題](assets/do-not-localize/github-issue.png)來提供檔案意見回饋

* 聯絡[客戶服務](https://experienceleague.adobe.com/?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [瞭解使用者介面](/help/using/user-interface.md)
>* [使用案頭應用程式](/help/using/using-desktop-app.md)
>* [在案頭應用程式中管理Assets](/help/using/assets-management-tasks.md)
