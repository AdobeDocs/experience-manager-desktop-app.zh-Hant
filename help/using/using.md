---
title: 使用 [!DNL Experience Manager] 案頭應用程式
description: 使用 [!DNL Adobe Experience Manager] 案頭應用程式，從您的Win或Mac案頭直接使用 [!DNL Adobe Experience Manager] DAM資產，並用於其他應用程式。
mini-toc-levels: 1
feature: Desktop App,Asset Management
exl-id: fa19d819-231a-4a01-bfd2-6bba6fec2f18
source-git-commit: fb11b41020a4c2b2c40e8adcde822c65a7fe8985
workflow-type: tm+mt
source-wordcount: '4734'
ht-degree: 0%

---

# 使用[!DNL Adobe Experience Manager]案頭應用程式 {#use-aem-desktop-app-v2}

使用[!DNL Adobe Experience Manager]案頭應用程式來存取儲存在本機案頭上[!DNL Adobe Experience Manager] DAM存放庫中的數位資產。 然後您就可以在任何案頭應用程式中使用這些資產。 您可以在案頭應用程式中在本機開啟及編輯資產。 進行變更後，請透過版本控制將它們上傳回[!DNL Experience Manager]以與其他使用者共用更新。 您也可以將新檔案和資料夾階層上傳到[!DNL Experience Manager]、建立資料夾，以及從[!DNL Experience Manager] DAM中刪除資產或資料夾。

整合可讓組織中的不同角色集中管理[!DNL Experience Manager Assets]中的資產，並在Windows或macOS上的原生應用程式中存取本機案頭上的資產。

當您在登出後或第一次開啟應用程式時，請以`https://[aem-server-url]:[port]/`格式提供您[!DNL Experience Manager]伺服器的URL。 然後選取[!UICONTROL Connect]選項。 提供認證以將應用程式連線至伺服器。

您使用[!DNL Adobe Experience Manager]案頭應用程式執行的主要工作為：

![您可以使用[!DNL Experience Manager]案頭應用程式完成的工作流程和工作](assets/aem_desktop_app_usecases_v2.png "您可以使用 [!DNL Adobe Experience Manager] 案頭應用程式完成的工作流程和工作")

<!--Download [this](assets/aem_desktop_app_usecases_print.pdf) print-ready PDF file.-->

## 案頭應用程式的運作方式 {#how-app-works2}

開始使用應用程式之前，請先瞭解[應用程式的運作方式](release-notes.md#how-app-works)。 此外，請熟悉下列詞語：

* **[!UICONTROL Desktop Actions]**：從Assets Web介面中，在瀏覽器內可探索資產位置或取出並開啟資產，以在原生案頭應用程式中編輯。 這些動作可從Web介面取得，並使用案頭應用程式功能。 請參閱[如何啟用案頭動作](using.md#desktopactions-v2)。

* 檔案狀態為&#x200B;**[!UICONTROL Cloud Only]**：這類資產未在本機電腦上下載，僅可在[!DNL Experience Manager]伺服器上使用。

* 檔案狀態為&#x200B;**[!UICONTROL Available locally]**：資產已下載，並可在本機電腦上使用。 資產不會變更。

* 檔案狀態為&#x200B;**[!UICONTROL Edited locally]**：此類資產已在本機修改，且變更仍會保留至已上傳至[!DNL Experience Manager]伺服器的檔案。 上傳之後，狀態會變更為[!UICONTROL Available locally]。 請參閱[編輯資產](using.md#edit-assets-upload-updated-assets)。

* 檔案狀態為&#x200B;**[!UICONTROL Editing conflict]**：如果您與其他人同時編輯資產，應用程式會指出發生編輯衝突。 應用程式也提供保留或捨棄變更的選項。 請參閱[如何避免編輯衝突](using.md#adv-workflow-collaborate-avoid-conflicts)。

* 檔案狀態為&#x200B;**[!UICONTROL Modified remotely]**：應用程式會指出您已下載的資產是否已在[!DNL Experience Manager]伺服器上變更。 應用程式也提供下載最新版本和更新本機復本的選項。 請參閱[如何避免編輯衝突](using.md#adv-workflow-collaborate-avoid-conflicts)。

* **[!UICONTROL Check-out]**：如果您正在編輯檔案或要編輯檔案，請切換狀態以簽出。 它會在應用程式和[!DNL Experience Manager]網頁介面的資產上新增鎖定圖示。 鎖定圖示會向其他使用者指示，以避免同時編輯相同的資產，因為這會導致編輯衝突。

* **[!UICONTROL Check-in]**：將資產標示為可供其他使用者編輯，而不會造成編輯衝突。 上傳變更時，鎖定圖示會自動移除。 切換籤入狀態也會移除鎖定圖示，不過Adobe建議您避免手動簽入而不上傳變更。 如果您捨棄變更，請手動切換入庫。

* **[!UICONTROL Open]**&#x200B;動作：只要開啟資產，即可在原生應用程式中預覽。 Adobe建議您避免使用此動作來編輯資產。 原因是它不會簽出資產。 同時，其他使用者也可以進行編輯，導致編輯衝突。

* **[!UICONTROL Open with]**&#x200B;動作： 「開啟方式」功能可讓您使用預設應用程式以外的特定應用程式開啟檔案。 這對於選擇偏好的程式、存取不同格式的檔案、疑難排解預設應用程式的問題，或使用多個程式非常有用。 它可讓您暫時覆寫預設應用程式，而不會永久變更設定，提供彈性。

* **[!UICONTROL Open In Web]**&#x200B;動作：若要在[!DNL Experience Manager]網頁介面中檢視資產，請在網頁中開啟該資產。 您可以從[!DNL Experience Manager]介面啟動更多工作流程，例如更新中繼資料或資產探索。

* **[!UICONTROL Edit]**&#x200B;動作：使用動作來修改影像。 按一下[!UICONTROL Edit]取出資產並在資產上新增鎖定圖示。 按一下「編輯」後，如果您不想編輯資產，請按一下[!UICONTROL Toggle check-in]。 若要刪除、重新命名或移動[!DNL Experience Manager] DAM資料夾階層中的資產，請使用[!DNL Experience Manager] Web介面動作，而非編輯動作。

* **[!UICONTROL Download]**&#x200B;動作：將資產下載到您的本機電腦。 您現在可以下載資產，稍後再進行編輯；離線工作稍後再上傳變更。 Assets會下載到檔案系統的快取資料夾中。

* **[!UICONTROL Reveal File]**&#x200B;或&#x200B;**[!UICONTROL Reveal Folder]**&#x200B;動作：將資產下載至本機快取資料夾時，應用程式會模擬本機網路磁碟機。 它提供每個資產的本機路徑。 若要知道此路徑，請使用應用程式中適當的顯示選項。 需要顯示動作才能在Creative Cloud應用程式中放置資產。 請參閱[置入資產](using.md#place-assets-in-native-documents)。

* **[!UICONTROL Delete]**&#x200B;動作：從[!DNL Experience Manager] DAM存放庫中刪除資產。 該動作會刪除Experience Manager伺服器上的資產原始副本。 如果您只想捨棄本機資產的修改，請參閱[捨棄變更](using.md#edit-assets-upload-updated-assets)。

* **[!UICONTROL Upload Changes]**：案頭應用程式只有在您明確上傳至[!DNL Experience Manager]伺服器時，才會上傳更新的資產。 當您儲存編輯時，變更只會儲存在本機電腦上。 上傳時，資產會自動入庫，且鎖圖示會移除。 請參閱[編輯資產](using.md#edit-assets-upload-updated-assets)。

## 在[!DNL Experience Manager]網頁介面中啟用案頭動作 {#desktopactions-v2}

從瀏覽器的[!DNL Assets]使用者介面中，您可以探索資產位置或取出並開啟資產，以在您的案頭應用程式中進行編輯。 這些選項稱為[!UICONTROL Desktop Actions]，預設不會啟用。 若要啟用此功能，請依照下列步驟執行。

1. 在[!DNL Assets]主控台中，按一下工具列中的&#x200B;**[!UICONTROL User]**&#x200B;圖示。
1. 按一下&#x200B;**[!UICONTROL My Preferences]**&#x200B;以顯示&#x200B;**[!UICONTROL Preferences]**&#x200B;對話方塊。

1. 在[!UICONTROL User Preferences]對話方塊中，選取&#x200B;**[!UICONTROL Show Desktop Actions For Assets]**，然後按一下&#x200B;**[!UICONTROL Accept]**。

   ![選取[顯示Assets的案頭動作]以啟用案頭動作](assets/enable_desktop_actions.png)

   *圖：選取[!UICONTROL Show Desktop Actions For Assets]以啟用案頭動作。*

## 檢視資產 {#view-assets}

AEM案頭應用程式可讓您以四種不同的檢視檢視檢視資產：

* **[!UICONTROL Show Assets]：**&#x200B;可讓您檢視所有資產。
* **[!UICONTROL Show Collections]：**&#x200B;可讓您檢視在原生AEM應用程式中建立的所有集合。 檢視更多[集合](#collections-desktop-app)。
* **[!UICONTROL Edited Locally]：**&#x200B;可讓您顯示所有本機修改的資產。 在此檢視中，您可以新增和上傳多個資產。
* **[!UICONTROL Asset transfers]：**&#x200B;可讓您檢視從原生應用程式傳輸到本機或反向傳輸的所有資產。
* **[!UICONTROL Pinned items]：**&#x200B;可讓您檢視所有釘選專案。

若要在AEM案頭應用程式的各種資產檢視中進行選擇，請執行以下步驟：

1. 開啟AEM案頭應用程式。

1. 前往右上方的下拉式清單檢視。 從可用的檢視中選擇一個。

   ![釘選或取消釘選資料夾](assets/view-pinned-assets.png)

### 檢視新新增的資料夾和檔案 {#view-newly-added-files-folders}

您可以從本機電腦將新建立的資產上傳到AEM，並在此儲存中央存放庫。 若要在本機檢視這些新建立的資產，請移至&#x200B;**[!UICONTROL View]**&#x200B;下拉式功能表，然後選取&#x200B;**[!UICONTROL Show Assets]**&#x200B;以檢視所有更新及其時間表和標題，或選取&#x200B;**[!UICONTROL Edited Locally]**。 這兩個選項都會明確顯示本機編輯的資產。

## 瀏覽、搜尋和預覽資產 {#browse-search-preview-assets}

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

## 資產管理 {#assets-management}

資產管理包括組織、維護和最佳化數位資產，以簡化工作流程。 它包含複製和重新命名檔案、釘選或取消釘選資料夾以快速存取，以及檢視各種版面配置中的資產等工作。 這有助於提高效率、簡化資產追蹤，並確保跨平台輕鬆擷取和組織數位資產。

### 複製檔案 {#duplicate-files}

當您想要保留原始檔案並在類似檔案上進行變更時，可以同時複製不同位置（本機與雲端）的檔案。 這可以透過跨資產重複檔案操作來完成。

若要在AEM案頭應用程式中複製檔案，請遵循下列步驟：

1. 瀏覽至資料夾並選取您要複製的資產。

   ![重複的檔案](assets/more-options.png)

1. 按一下&#x200B;**[!UICONTROL More actions]** ![更多動作圖示](assets/do-not-localize/more2_da2.png)並選取![重複圖示](assets/do-not-localize/duplicate.svg) **[!UICONTROL Duplicate File]**&#x200B;動作。

1. 系統會以相同的檔案名稱和內容建立重複的檔案。

### 重新命名資產的標題 {#rename-asset-title}

若要重新命名資產的標題，請執行下列步驟：

1. 瀏覽您要重新命名的資產。

1. 按一下&#x200B;**[!UICONTROL More actions]** ![更多動作圖示](assets/do-not-localize/more2_da2.png)並選取&#x200B;**[!UICONTROL Rename]**&#x200B;以新增您想要的資產標題。

<!--1. Click **[!UICONTROL More actions]** ![More actions icon](assets/do-not-localize/more2_da2.png) and select **[!UICONTROL open in web]** to open the asset in its native application.

1. Go to asset details. Under [!UICONTROL Basic] tab, go to title and enter the text.-->

### 釘選或取消釘選資料夾 {#pin-unpin-folder}

若要快速存取，您可以執行下列步驟來釘選或取消釘選資料夾：

1. 瀏覽您要釘選或取消釘選的資產。

1. 按一下&#x200B;**[!UICONTROL More actions]** ![更多動作圖示](assets/do-not-localize/more2_da2.png)並選取[!UICONTROL pin]以釘選資產或資料夾。 或者，按一下[!UICONTROL unpin]以取消釘選。

   ![釘選或取消釘選資料夾](assets/pin-unpin.png)

### 自動重新整理 {#auto-refresh}

自動重新整理功能會即時自動更新內容，確保您一律看到最新資訊，不會手動重新載入頁面。 執行以下步驟來自動重新整理資產，以取得已更新資產的清單：

1. 開啟AEM案頭應用程式。

1. 按一下功能表列上的![重新整理圖示](assets/do-not-localize/refresh.png)以取得更新。

## 下載資產 {#download-assets}

您可以下載本機檔案系統上的資產。 應用程式會從[!DNL Experience Manager]伺服器擷取資產，並將相同的復本儲存在本機檔案系統上。

按一下&#x200B;**[!UICONTROL More actions]** ![更多選項圖示](assets/do-not-localize/more2_da2.png)取得選項，然後按一下![下載圖示](assets/do-not-localize/download_cloud_da2.png)進行下載。

![資產下載選項](assets/download_option_da2.png "資產下載選項")

>[!NOTE]
>
>下載或上傳大型檔案或多個檔案時，應用程式會關閉對資產和資料夾的動作。 下載或上傳完成時，這些動作即可使用。

如果佇列大小很大或您遇到一些網路問題，下載多個資產可能會導致效能不佳。 此外，當您下載資料夾時，可能會無意中將許多資產排入下載佇列。 為避免冗長的等候時間，應用程式會限制單次下載的資產數量。 若要瞭解如何進行設定，請參閱[設定偏好設定](install-upgrade.md#set-preferences)。 即使低於此限制，應用程式有時也可能會在下載明顯大型的資料夾之前尋求確認。

![應用程式確認下載相對大量資產](assets/download_confirmation_da2.png "應用程式確認下載相對大量資產")

如果選取並下載資料夾，應用程式只會下載直接儲存在[!DNL Experience Manager]中資料夾中的資產。 它不會自動從子資料夾中下載資產。

## 在案頭上開啟資產 {#openondesktop-v2}

您可以開啟遠端資產，以便在原生應用程式中檢視。 資產會下載至本機資料夾。 然後，它們會在與檔案格式相關的原生應用程式中啟動。 您可以變更原生應用程式，以在Mac或Windows中開啟特定檔案型別（副檔名）。

按一下資產功能表中的&#x200B;**[!UICONTROL Open]**。 資產會從本機下載，並以原生應用程式開啟。 檢查狀態列中大型資產的下載進度和傳輸速度。

<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")
-->

>[!NOTE]
>
>如果預期變更未反映在應用程式中，請按一下重新整理圖示![重新整理圖示](assets/do-not-localize/refresh.png)，或在應用程式介面中按一下滑鼠右鍵，然後按一下&#x200B;**[!UICONTROL Refresh]**。 進行較大型的下載或上傳時，無法使用這些動作。

若要開啟資產的本機下載資料夾，請按一下![更多動作圖示](assets/do-not-localize/more2_da2.png)，然後按一下![顯示圖示](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]**&#x200B;動作。

## 集合 {#collections-desktop-app}

AEM案頭應用程式可讓您[檢視](#view-collections-desktop-app)、[下載](#download-collections-desktop-app)，並瀏覽在[!DNL Adobe Experience Manager Assets]應用程式上建立的集合。

### 檢視集合 {#view-collections-desktop-app}

執行以下步驟，在案頭應用程式中檢視集合：

1. 開啟AEM案頭應用程式並移至[檢視資產](#view-assets)。

1. 選取&#x200B;**[!UICONTROL Show Collections]**。 會顯示原生應用程式上可用的集合。

   ![集合案頭應用程式](assets/collections-desktop-app.png)

### 下載集合 {#download-collections-desktop-app}

執行以下步驟，在案頭應用程式中下載集合：

1. 請依照[檢視集合](#view-collections-desktop-app)中顯示的步驟1和2操作。

1. 前往更多動作![更多動作圖示](assets/do-not-localize/more2_da2.png)在您要下載的集合上。

1. 按一下&#x200B;**[!UICONTROL Download]**&#x200B;下載特定集合。

## 使用中繼資料結構建立資料夾 {#create-folder-with-metadata-schema}

您可以使用AEM案頭應用程式，在建立新資料夾時指派中繼資料。 要執行此操作，請執行下列步驟：

1. 前往建立目錄圖示![新增資料夾圖示](assets/do-not-localize/add-folder.svg)。 出現&#x200B;**[!UICONTROL Create Directory]**&#x200B;畫面。

1. 新增下列詳細資料：
   * 資料夾的&#x200B;**[!UICONTROL Name]**。
   * **[!UICONTROL Folder Metadata Schema]**&#x200B;以選擇資料夾的中繼資料階層，或如果您不想讓任何中繼資料與其產生關聯，則選擇&#x200B;**[!UICONTROL none]**。

1. 按一下&#x200B;**[!UICONTROL OK]**&#x200B;以繼續進行。

## 使用資產或將資產放入原生檔案 {#place-assets-in-native-documents}

在某些情況下，例如將資產放入原生檔案時，您可以在Windows檔案總管或Mac Finder中存取檔案。 若要移至本機下載檔案的檔案系統位置，請使用![顯示圖示](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]**&#x200B;選項。

![顯示資產的檔案動作](assets/revealfile_action_da2.png "顯示資產的檔案動作")

按一下資料夾上的&#x200B;**[!UICONTROL Reveal File]**&#x200B;或&#x200B;**[!UICONTROL Reveal Folder]**，以使用本機電腦上預先選取的檔案或資料夾開啟Windows檔案總管或Mac Finder。 例如，在支援放置或連結本機檔案的原生應用程式中放置[!DNL Experience Manager]檔案時，選項很有用。 若要瞭解如何在Adobe InDesign中放置檔案，請參閱[放置圖形](https://helpx.adobe.com/tw/indesign/using/placing-graphics.html)。

**[!UICONTROL Reveal File]**&#x200B;動作會開啟本機網路共用。 它只會顯示本機可用的資產。 也就是說，會顯示使用應用程式揭露、下載或開啟/編輯的資產。 本機網路共用沒有上傳任何變更到[!DNL Experience Manager]。 若要上傳變更，請明確使用應用程式中的&#x200B;**[!UICONTROL Upload Changes]**&#x200B;或&#x200B;**[!UICONTROL Upload]**&#x200B;動作。

>[!NOTE]
>
>為了與[!DNL Experience Manager]案頭應用程式v1.x回溯相容，顯示的檔案是從本機網路共用提供，只會公開本機可用的檔案。 顯示檔案的案頭路徑與應用程式v1.x建立的路徑相同。

>[!CAUTION]
>
>請勿使用&#x200B;**[!UICONTROL Reveal File]**&#x200B;選項編輯原生應用程式中的資產。 請改用&#x200B;**[!UICONTROL Edit]**&#x200B;動作。 若要瞭解更多資訊，請參閱[進階工作流程：共同作業相同的檔案，避免編輯衝突](#adv-workflow-collaborate-avoid-conflicts)。

## 編輯資產並將更新的資產上傳到[!DNL Experience Manager] {#edit-assets-upload-updated-assets}

當您想要進行變更並將更新的資產上傳到[!DNL Experience Manager]伺服器時，請開啟要編輯的資產。 為避免與其他使用者的編輯發生衝突，請使用應用程式來起始編輯工作階段。 開始編輯之前，請確定資產上沒有鎖定圖示，表示有其他使用者正在編輯資產。

若要編輯資產，請搜尋資產或瀏覽至資產位置。 按一下![其他圖示](assets/do-not-localize/more2_da2.png)並按一下&#x200B;**[!UICONTROL Edit]**。

使用&#x200B;**[!UICONTROL Toggle Check-out]**&#x200B;鎖定資產，以防止在下列兩種情況下與其他使用者的編輯發生衝突：

* 您已開始編輯資產，但未先將資產出庫（例如，直接開啟資產）。
* 您打算儘快開始編輯資產，不希望其他人編輯。

完成編輯後，應用程式會顯示已變更資產的&#x200B;**[!UICONTROL Edited Locally]**&#x200B;狀態。 儲存至資產的所有變更僅在本機進行，直到您將變更上傳至[!DNL Experience Manager]為止。 若要逐一上傳個別或數個資產，請從資產的選項中按一下&#x200B;**[!UICONTROL Upload Changes]**。 它會在[!DNL Experience Manager]中建立資產的版本。 使用[!DNL Assets]的Web介面，您可以在[時間軸檢視](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-65/content/assets/using/activity-stream)中看到資產歷史記錄。

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

<!--### Upload local file to AEM {#upload-local-file-to-aem}-->


### 管理資產名稱中的特殊字元 {#special-characters-in-filename}

在舊版應用程式中，在存放庫中建立的節點名稱會保留使用者提供的資料夾名稱空格和大小寫。 若要讓目前應用程式模擬v1.10應用程式的節點命名規則，請在[!UICONTROL Preferences]中啟用[!UICONTROL Use legacy conventions when creating nodes for assets and folders]。 檢視[應用程式偏好設定](/help/using/install-upgrade.md#set-preferences)。 此舊版偏好設定預設為停用。

>[!NOTE]
>
>應用程式只會使用下列命名慣例變更存放庫中的節點名稱。 應用程式會保留資產的`Title`不變。

<!-- TBD: Do NOT use this table.

| Where do characters occur | Characters | Legacy preference | Renaming convention | Example |
|---|---|---|---|---|
| In file name extension | `.` | Enabled or disabled | Retained as is | NA |
| File or folder name | `. / : [ ] | *` | Enabled or disabled | Replaced with a `-` (hyphen) | `myimage.jpg` remains as is and `my.image.jpg` changes to `my-image.jpg`. |
| Folder name | `% ; # , + ? ^ { } "` | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | `% # ? { } &` | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | Whitespaces | Enabled or disabled | Retained as is | NA |
| Folder name | Whitespaces | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | Uppercase characters | Disabled | Retained as is | tbd |
| Folder name | Uppercase characters | Disabled | Replaced with a `-` (hyphen) | tbd |
-->

| 字元‡ | 應用程式中的舊版偏好設定 | 當出現在檔案名稱中 | 當出現在資料夾名稱中時 | 範例 |
|---|---|---|---|---|
| `. / : [ ] \| *` | 啟用或停用 | 已取代為`-` （連字型大小）。 副檔名中的`.` （點）會維持原狀。 | 已取代為`-` （連字型大小）。 | `myimage.jpg`保持原狀，且`my.image.jpg`變更為`my-image.jpg`。 |
| `% ; # , + ? ^ { } "`和空格 | ![取消選取圖示](assets/do-not-localize/deselect-icon.png)已停用 | 保留空格 | 已取代為`-` （連字型大小）。 | `My Folder.`變更為`my-folder-`。 |
| `# % { } ? & .` | ![取消選取圖示](assets/do-not-localize/deselect-icon.png)已停用 | 已取代為`-` （連字型大小）。 | 不適用 | `#My New File.`變更為`-My New File-`。 |
| 大寫字 | ![取消選取圖示](assets/do-not-localize/deselect-icon.png)已停用 | 大小寫維持原狀。 | 變更為小寫字元。 | `My New Folder`變更為`my-new-folder`。 |
| 大寫字 | ![選取專案核取圖示](assets/do-not-localize/selection-checked-icon.png)已啟用 | 大小寫維持原狀。 | 大小寫維持原狀。 | 不適用 |

‡字元清單是以空格分隔的清單。

<!-- TBD: Check if the following is to be included in the footnote.

Do not use &#92;&#92; in the names of files and &#92;&#116; &#38; in the names of folders. 
-->


<!-- TBD: Securing the below presentation of the same content in a comment.

**File names**

| Characters | Replaced by |
|---|---|
| &#35; &#37; &#123; &#63; &#125; &#38; &#46; &#47; &#58; &#91; &#124; &#93; &#42; | hyphen (-) |
| whitespaces | whitespaces are retained |
| capital case | casing is retained |

>[!CAUTION]
>
>Avoid using &#92;&#92; in file names.

**Folder names**

| Characters | Replaced by |
|---|---|
| Characters | Replaced by |
| &#37; &#59; &#35; &#44; &#43; &#63; &#94; &#123; &#123; &#34; &#46; &#47; &#59; &#91; &#93; &#124; &#42; | hyphen (-) |
| whitespaces | hyphen (-) |
| capital case | lower case |

>[!CAUTION]
>
>Avoid using &#92;&#92; &#92;&#116; &#38; in folder names.

>[!NOTE]
>
>If you enable [!UICONTROL Use legacy conventions when creating nodes for assets and folders] in app [!UICONTROL Preferences], then the app emulates v1.10 app behavior when uploading folders. In v1.10, the node names created in the repository respect spaces and casing of the folder names provided by the user. For more information, see [app Preferences](/help/using/install-upgrade.md#set-preferences).

-->

## 使用多個資產 {#work-with-multiple-assets}

使用者可以透過動作（例如一次上傳所有編輯內容，或按幾下上傳巢狀資料夾）輕鬆處理和管理多個資產。

### 瀏覽大型資料夾 {#browse-large-folders}

使用包含許多資產的檔案夾時，請捲動以檢視更多資產。 若要使用鍵盤捲動，請按幾次Tab鍵以選取頂端的資產。 請注意醒目提示的資產，以知道何時選取它。 現在請使用向下鍵在資產清單中移動。

### 所選資產的快速動作 {#quick-actions-for-selected-assets}

按一下一些資產的縮圖以選取資產。 若要選取所有資產，請按一下應用程式頂端列中的核取方塊。 一組適用於所有已選取資產的動作會一起顯示在應用程式底部的工具列中。

![底部的工具列顯示與選取的資產相關的動作](assets/actions_bottom_toolbar1_da2.png "底部的工具列顯示選取資產的常用動作")

![選取範圍沒有通用動作時，工具列中沒有動作](assets/actions_bottom_toolbar2_da2.png "選取範圍沒有通用動作時，工具列不會顯示任何動作。")

底部工具列中的可用動作取決於所選檔案的狀態。 例如，如果您只選取&#x200B;**[!UICONTROL Edited Locally]**&#x200B;個檔案，您會看到&#x200B;**[!UICONTROL Upload Changes]**&#x200B;圖示。 如果您選取&#x200B;**[!UICONTROL Edited locally]**&#x200B;和&#x200B;**[!UICONTROL Cloud only]**&#x200B;的混合，**[!UICONTROL Upload Changes]**&#x200B;動作將不可用。

### 尋找所有已編輯的影像 {#find-all-edited-images}

應用程式會提供一個名為&#x200B;**[!UICONTROL Edited locally]**&#x200B;的檢視，讓您快速存取所有您在本機下載的檔案（透過[!UICONTROL Open]或[!UICONTROL Edit]動作），然後再修改。 應用程式可讓您選取所有在本機編輯的資產，並按幾下滑鼠即可上傳變更。 此檢視也會顯示有編輯衝突的本機編輯資產。

![篩選以檢視所有本機編輯的資產](assets/edited_locally_filter_da2.png "例如，篩選以檢視所有本機編輯的資產以進行大量編輯上傳")

### 大量上傳資產 {#bulk-upload-assets}

使用者或組織（例如攝影師或創意代理商）可在拍攝、潤飾或從較大集合中選取等活動中建立許多本機資產。 這些工作通常在[!DNL Experience Manager]之外完成。 他們可以直接從案頭應用程式上傳這些大型本機資料夾到[!DNL Assets]。 會保留資料夾階層，並上傳所有巢狀子資料夾和包含的資產。 相同伺服器的其他使用者也可以立即使用上傳的資產。 Assets會在背景上傳，因此操作不會繫結至網頁瀏覽器工作階段。

![從您的案頭大量上傳多個本機資料夾到[!DNL Experience Manager]](assets/upload_local_folders_da2.png "從您的案頭大量上傳多個本機資料夾到Experience Manager")

上傳後，如果預期變更未反映在應用程式中，請按一下重新整理圖示![重新整理圖示](assets/do-not-localize/refresh.png)。

>[!NOTE]
>
>請勿使用上傳功能跨兩個[!DNL Experience Manager]部署移轉資產。 請參閱[移轉指南](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-65/content/assets/administer/assets-migration-guide)。

### 已轉移資產的清單 {#list-of-transferred-assets}

若要檢視指定工作階段中傳輸的資產清單，請參閱[將資產上傳至 [!DNL Experience Manager]](#upload-and-add-new-assets-to-aem)。

## 進階工作流程：從[!DNL Assets]網頁介面開始 {#adv-workflow-start-from-aem-ui}

如有需要，請從Assets網頁介面啟動您的工作流程。 案頭應用程式會與[!DNL Experience Manager]整合，以便在使用「案頭動作」提出要求時接管。

從Web介面啟動工作流程的一個特殊情況是資產探索。 Assets使用者介面中的Omnisearch列提供豐富而進階的搜尋體驗。 您可能想要先在網頁上找到想要的資產，然後使用[!UICONTROL Desktop Actions]在應用程式中啟動工作流程。 某些範例案例包含使用Facet篩選搜尋結果、尋找從Adobe Stock授權的特定資產，或貴組織實作的自訂，以便您更妥善地從Web介面探索。

當您嘗試在Assets網頁介面上執行下列動作時，就會使用案頭應用程式功能：

* 允許[!UICONTROL Open]、[!UICONTROL Edit]和[!UICONTROL Reveal]的[!UICONTROL Desktop Actions]
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

## 進階工作流程：在相同檔案上共同作業並避免編輯衝突 {#adv-workflow-collaborate-avoid-conflicts}

在合作環境中，多位使用者可能會使用相同的資產集，這可能會導致版本設定衝突。 若要避免衝突，請遵循下列最佳實務：

* 按一下[!UICONTROL Open]不要編輯任何資產。 請勿透過從檔案系統資料夾中開啟來編輯本機下載的資產。 其他使用者不知道資產正在編輯中。
* 若要編輯資產，請一律按一下[!UICONTROL Edit]。 它會在原生應用程式中開啟資產，並在資產上新增鎖定圖示，讓其他使用者知道資產正在編輯中。
* 如果您不小心開始編輯而未按一下[!UICONTROL Edit]，請按一下[!UICONTROL Toggle Check-in]。 此功能會將鎖定圖示新增至資產。 即使您計畫稍後編輯資產，但想避免其他人編輯它，請按一下「[!UICONTROL Toggle Check-in]」以鎖定資產。
* 在編輯資產之前，請確定其他使用者未編輯該資產。 尋找資產上的鎖定圖示。
* 完成編輯後，請上傳所有變更，然後入庫資產。

![編輯衝突狀態](assets/edits_conflicts_status_da2.png "編輯衝突狀態")

如果本機下載的資產在[!DNL Experience Manager]伺服器上更新，應用程式會顯示&#x200B;**[!UICONTROL Modified remotely]**&#x200B;狀態。 您可以分別按一下[!UICONTROL Remove]或[!UICONTROL Update]，移除本機復本或重新整理本機復本。 對話方塊中的連結可讓您檢視資產的兩個版本。

![遠端修改資產時解決衝突的選項](assets/modified_remotely_dialog_da2.png "遠端修改資產時解決衝突的選項")

如果您在本機編輯的資產也在您不知情的情況下在伺服器上更新，應用程式會顯示&#x200B;**[!UICONTROL Editing Conflict]**&#x200B;狀態。 您可以保留一組變更 — 保留您的更新（按一下&#x200B;**[!UICONTROL Keep Mine]**）並刪除其他使用者的編輯，或遵循其他使用者的更新並刪除您的更新(**[!UICONTROL Overwrite Mine]**)。

![解決編輯衝突的選項](assets/editing_conflict_dialog_da2.png "解決編輯衝突的選項")

## 進階工作流程：在InDesign檔案中放置和連結資產 {#adv-workflow-place-assets-indesign}

當您使用[!DNL Experience Manager]案頭應用程式開啟含有連結資產的檔案時，資產會預先下載，並顯示在原生應用程式中。 為了讓此工作流程正常運作，您的原生應用程式必須支援放置本機資產的連結，且[!DNL Experience Manager]必須支援將二進位檔案中的這些連結解析為伺服器端參考。

[!DNL Experience Manager]案頭應用程式可支援此工作流程，包含一些特定的Adobe Creative Cloud案頭應用程式和檔案格式 — Adobe InDesign、Adobe Illustrator和Adobe Photoshop。 工作流程可讓您有效率地使用支援的Creative Cloud檔案。 如果使用者A將資產新增至InDesign檔案並將它簽入[!DNL Experience Manager]，則使用者B可以看到檔案中的資產，即使它們不屬於該檔案的一部分。 資產會從使用者B的電腦本機下載。

>[!NOTE]
>
>案頭應用程式可對應至Windows上的任何磁碟機。 不過，若要順利作業，請勿變更預設磁碟機代號。 如果相同組織的使用者使用不同的磁碟機代號，則他們看不到其他人置入的資產。 路徑變更時不會擷取已放置的資產。 置入的資產會繼續置於二進位檔案（例如INDD）中，且不會移除。

若要瞭解此工作流程的限制，請參閱[系統需求和支援的版本](release-notes.md)。

若要使用影像資產和InDesign嘗試此工作流程，請遵循下列步驟：

1. 在[!DNL Experience Manager]中保留已放置資產的INDD檔案。 若要瞭解如何建立此類INDD檔案，請參閱[放置圖形](https://helpx.adobe.com/tw/indesign/using/placing-graphics.html)。
1. 從案頭應用程式內，**[!UICONTROL Edit]**&#x200B;在[!DNL Experience Manager]中置入資產的INDD檔案。
1. 應用程式會下載InDesign檔案和連結的資產。 當InDesign開啟檔案時，連結會得到解析、資產會下載，而資產會顯示在InDesign檔案中。
1. 若要在InDesign檔案中放置新圖形，請對資產使用&#x200B;**[!UICONTROL Reveal File]**&#x200B;動作。 此動作會在本機下載資產，並在Windows檔案總管或Mac Finder中開啟本機網路共用位置。
1. 將顯示的資產放入InDesign檔案中。 這樣做會在檔案中建立連結。
1. 完成InDesign檔案中的編輯後，請儲存並使用案頭應用程式將其上傳至[!DNL Experience Manager]。

## 進階工作流程：在本機下載資產 {#adv-workflow-download-assets-locally}

應用程式經常從[!DNL Experience Manager]伺服器下載資產到您的本機檔案系統。 下載耗用頻寬和磁碟空間。 瞭解情況有助於您最佳化完成下載的等待時間。

您可以隨選從應用程式內下載資產。 請參閱[下載資產](#download-assets)。

當您使用[!UICONTROL Open]動作在原生案頭應用程式中開啟資產時，如果資產尚未在本機提供，則會下載到本機。 請參閱[開啟資產](#openondesktop-v2)。

當您從應用程式內顯示資產或資料夾的位置時，資產或資料夾會先在本機下載，然後在您電腦上的本機網路共用中開啟。 請參閱[開啟資產](#openondesktop-v2)。

當您使用[!UICONTROL Edit]動作編輯原生案頭應用程式中的資產時，如果資產尚未在本機提供，則會下載到本機。 檢視[編輯資產並將更新的資產上傳到 [!DNL Experience Manager]](#edit-assets-upload-updated-assets)。

如果應用程式已安裝並獲准使用，它會在您從[!DNL Experience Manager]網頁介面使用[!UICONTROL Desktop Actions]時完成動作。 應用程式會先下載資產，然後完成動作。
