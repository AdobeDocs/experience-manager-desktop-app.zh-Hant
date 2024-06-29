---
title: 使用 [!DNL Experience Manager] 案頭應用程式1.10版。
description: 瞭解如何使用Adobe Experience Manager案頭應用程式1.10版，並使用案頭上的資產最佳化您的工作。
feature: Desktop App,Asset Management
exl-id: 2fdc1c8d-b822-4cca-ad06-bd875a00aa6d
source-git-commit: 5676e7ece8bb43f051dae72d17e15ab1c34caefc
workflow-type: tm+mt
source-wordcount: '2329'
ht-degree: 0%

---

# 使用 [!DNL Experience Manager] 案頭應用程式v1.10 {#use-aem-desktop-app-v1x}

使用應用程式時，此應用程式內的 [!DNL Experience Manager] 可在您的本機案頭上輕鬆存取，並可用於任何案頭應用程式。 Assets可以輕鬆地在Mac Finder或Windows檔案總管中顯示、在案頭應用程式中開啟，並在本機變更 — 變更會儲存回 [!DNL Experience Manager] 存放庫中建立新版本。

此整合可跨Creative Cloud和其他應用程式啟用集中資產管理和存取，確保符合品牌和其他標準。

您使用進行的主要工作 [!DNL Experience Manager] 案頭應用程式v1包含：

1. [使用 [!DNL Experience Manager] 伺服器](#installandconnect)
1. [直接在案頭應用程式上開啟資產](#openondesktop)
1. [從案頭應用程式編輯及簽出資產](#workonassets)
1. [大量上傳資產和資料夾](#bulkupload)

如需各種建議的優點和缺點，請參閱 [使用案頭應用程式的最佳作法](best-practices-for-v1.md). 如果您在使用應用程式時遇到問題，請參閱如何 [疑難排解 [!DNL Experience Manager] 案頭應用程式](troubleshoot-app-v1.md).

>[!NOTE]
>
>在中推出案頭應用程式 [!DNL Experience Manager] 6.1版，並被稱為 [!DNL Experience Manager Assets Companion App].

## [!DNL Experience Manager] 創意工作流程中的案頭應用程式接觸點 {#aem-desktop-app-touch-points-in-the-creative-workflow}

[!DNL Experience Manager] 案頭應用程式，以及 [!DNL Assets]，整合您的創意工作流程中，並提供下列接觸點。

![[!DNL Experience Manager] 案頭應用程式接觸點創意工作流程](assets/aem_desktopapp_workflow.png)

[!DNL Experience Manager] 案頭應用程式接觸點創意工作流程

## 安裝應用程式並將其連線至 [!DNL Experience Manager] 伺服器 {#installandconnect}

開始建立或編輯創意資產之前，請先將案頭應用程式與 [!DNL Assets] 伺服器下載和上傳存放庫中的資產。 執行下列工作：

1. [安裝應用程式](#installapp).
1. [設定您的偏好設定](#inapppref) 和連線詳細資料。
1. [連線到 [!DNL Experience Manager] 伺服器](#connect) 並將資產存放庫掛接為本機磁碟機。
1. [啟用案頭動作](#desktopactions) 於 [!DNL Experience Manager] 伺服器。

此 [!DNL Experience Manager] 案頭應用程式使用HTTPS連線來連線至 [!DNL Experience Manager] 伺服器，以穩固且安全地傳輸您的資產。

>[!NOTE]
>
>對於所有或部分安裝和設定步驟，您可能需要您的 [!DNL Experience Manager] 管理員或系統管理員。

### 安裝應用程式 {#installapp}

確認應用程式支援您版本的Experience Manager伺服器，以便使用Experience Manager案頭應用程式。 下載適用於您作業系統(Mac或Windows)的安裝檔案（二進位檔），然後安裝應用程式。

視您的網路和系統偏好設定而定，可能需要詳細設定。 另請參閱 [安裝與設定 [!DNL Experience Manager] 案頭應用程式](install-configure-app-v1.md) 以取得更多詳細資料。

1. 前往 [[!DNL Experience Manager] 案頭應用程式v1.10下載頁面](/help/using/release-notes-of-v1.md) 並下載適合您作業系統的二進位檔。
1. 啟動下載的安裝檔案，然後依照畫面上的指示安裝應用程式。

   >[!NOTE]
   >
   >只有一個例項 [!DNL Experience Manager] 案頭應用程式可以一次安裝並啟用。

### 瞭解應用程式內選項和偏好設定 {#inapppref}

應用程式允許設定從進行連線和中斷連線 [!DNL Experience Manager] 伺服器、檢視上傳狀態、管理本機快取等。 預設設定適用於應用程式的典型使用者。 您可以調整設定，讓應用程式發揮更大效用。 此外，更充分運用與的整合 [!DNL Experience Manager] 伺服器。 以下是各種設定：

**探索Assets** 開啟本機磁碟機 [!DNL Assets] 存放庫已裝載。 換句話說，就是要探索現在可供本機電腦使用的資產。

**檢視資產狀態** 上傳已變更的資產或將新資產新增至 [!DNL Assets] 存放庫時，應用程式會在背景上傳資產。 背景上傳可讓您順利作業，不必等待上傳完成，尤其是大型資產。 您可以在本機儲存變更並忘記。 應用程式會花一些時間將這些資產傳送至伺服器，視可用的頻寬而定。 您可以檢查上傳的狀態，以及一些更基本的資訊。

**選項** 按一下案頭應用程式匣中的選項，將應用程式設定為在啟動時啟動，請連線至 [!DNL Experience Manager] 伺服器啟動時，並變更本機磁碟機代號 [!DNL Assets] 掛載之後。

**進階>管理快取** 您可以控制可用於本機快取的磁碟空間量。 來自的成品 [!DNL Assets] 伺服器會快取在本機，以獲得更流暢的體驗。 您可以變更預設值以符合您的需求。 此外，您也可以清除快取，以重新擷取所有資產。 當您清除快取時，它會保留您未儲存的變更。 任何未簽入的資產 [!DNL Experience Manager] 伺服器會保留且不會刪除。

### 連線到 [!DNL Experience Manager] 伺服器 {#connect}

應用程式支援Mac和Windows上的Proxy設定。 應用程式啟動時會讀取設定。 如果您修改Proxy設定，請重新啟動應用程式，變更才會生效。

>[!NOTE]
>
>如果您修改Proxy設定，請重新啟動應用程式，變更才會生效。 否則，應用程式會繼續使用先前設定的Proxy伺服器。

1. 啟動 [!DNL Experience Manager] 案頭應用程式。 對應您的 [!DNL Experience Manager] 使用應用程式的例項，指定您的 [!DNL Experience Manager] server，格式為 `https://[aem-server-url]:[port]`.

   ![在Mac上進行驗證並提供 [!DNL Experience Manager] 伺服器URL](assets/aem_desktop_app_server_url.png)

1. 在登入畫面中，指定執行個體的使用者名稱和密碼。 若要指定替代專案，請執行下列步驟： [!DNL Experience Manager] 執行個體，選取 **[!UICONTROL Alternate Login URL]** 選項。

   ![提供 [!DNL Experience Manager] 開啟登入畫面上的伺服器認證 [!DNL Experience Manager] 案頭應用程式](assets/login_screen_v1.png)

### 在中啟用案頭動作 [!DNL Experience Manager] 網頁介面 {#desktopactions}

從Assets使用者介面中，您可以探索資產位置或取出並開啟資產，以在您的案頭應用程式中編輯。 這些選項稱為案頭動作，預設不會啟用。 請依照下列步驟加以啟用。

1. 在Assets介面中，按一下/點選工具列右上角的「使用者」圖示。
1. 按一下 **[!UICONTROL My Preferences]** 以顯示 **[!UICONTROL Preferences]** 對話方塊。

   ![[!DNL Experience Manager] 使用使用者偏好設定的介面](assets/aem_ui_user_preferences.png)

1. 在 [!UICONTROL User Preferences] 對話方塊，選取 **[!UICONTROL Show Desktop Actions For Assets]**，然後按一下 **[!UICONTROL Accept]**.

   ![檢查 [!UICONTROL Show Desktop Actions For Assets] 啟用案頭動作](assets/enable_desktop_actions.png)

   *圖：檢查 [!UICONTROL Show Desktop Actions For Assets] 以啟用案頭動作。*

## 存取和開啟您案頭上的資產 {#openondesktop}

當您按一下 **開啟** 若要在本機電腦上開啟資產，應用程式會將資產下載至其內部快取。 應用程式會啟動與已下載資產檔案型別關聯的原生案頭應用程式。

在Mac上，選取 **開啟** ，以透過開啟資產 [!DNL Experience Manager] 案頭應用程式。 在Windows上，從快顯選單中選取「在網頁上開啟」以開啟資產。 從「資產狀態」視窗，按一下/點選 ![在案頭上開啟圖示](assets/do-not-localize/aemassets_icon_openondesktop.png) 以開啟資產。

針對Adobe InDesign (INDD)檔案，選取 **[!UICONTROL Open]** 從內容功能表。 當您按一下此選項時，應用程式會將連結的資產下載至您的本機檔案系統，然後在Adobe InDesign中開啟INDD檔案。 此方法可確保編輯INDD檔案時必要的資產在本機可供使用。

![使用來存取和開啟資產的內容功能表選項 [!DNL Experience Manager] 案頭應用程式](assets/aem_desktopapp_mac_context_menu.png)

*圖：內容功能表選項，用於存取和開啟使用 [!DNL Experience Manager] 案頭應用程式。*

>[!NOTE]
>
>Adobe建議您前往Mac上的「尋找器檢視選項」 ，並停用選項 **顯示專案資訊**， **顯示專案預覽**、和 **顯示預覽欄** 針對已掛載的 [!DNL Assets] 資料夾。 這可改善效能。

### 中的其他選項 [!DNL Experience Manager] 介面 {#additional-options-in-aem-assets}

在您對應 [!DNL Assets] 存放庫至您的本機磁碟機，您可以啟用其他圖示，並為對應的資產和資料夾顯示資料夾上傳功能。

1. 開啟 [!DNL Assets] 介面並將指標暫留在資料夾或資產上，以將案頭動作顯示為卡片檢視中的快速動作。

   ![在Assets UI中，開啟快速動作功能表以檢視案頭動作](assets/desktop_actions_in_card_view.png)

   *圖：在Assets UI中，開啟快速動作功能表以檢視案頭動作。*

   按一下 **案頭動作** 中選取資產後工具列中的選項，或從資產頁面的工具列中選取。

1. 若要在案頭應用程式中開啟與特定副檔名相關聯的資產，請按一下 **在案頭上開啟** 快速動作 ![在案頭上開啟圖示](assets/do-not-localize/aemassets_icon_openondesktop.png).

   或者，選擇 **開啟** 從 **案頭動作** 功能表。

若要在本機檔案系統上尋找特定資產，請按一下 **顯示** 快速動作 ![顯示圖示](assets/do-not-localize/aemassets_reveal_icon.png). 或者，選擇 **顯示** 從 **案頭動作** 功能表。

## 瞭解資產狀態 {#understand-the-asset-statuses}

| ![Windows預設應用程式圖示](assets/do-not-localize/win_default.png) | 應用程式已連線至伺服器，且所有資產都已同步。 |
--- |--- |
| ![Windows已停用的圖示](assets/do-not-localize/win_disabled.png) | 應用程式已啟動，但未連線至伺服器。 某些資產可能正在等候同步處理。 |
| ![Windows檔案同步圖示](assets/do-not-localize/win_sync.png) | Assets正在同步處理。 檔案正在上傳或下載。 您可以從「資產狀態」視窗檢視確切的狀態並暫停傳輸。 |
| ![Windows重新連線圖示](assets/do-not-localize/win_refresh.png) | 應用程式正在嘗試重新連線。 網路問題可能會導致其中斷連線。 |

## 使用您的資產 {#workonassets}

### 從簽出資產 [!DNL Experience Manager] 網頁介面 {#check-out-assets-from-the-aem-web-interface}

[!DNL Experience Manager Assets] 可讓您簽出資產以進行編輯，並在完成變更後重新簽入。 出庫資產後，只有您可以編輯、註釋、發佈、移動或刪除資產。 將資產出庫會鎖定資產，並防止其他使用者執行任何這些操作。 若要能夠簽出/簽入資產，您需要這些資產的寫入許可權。

有兩種方式可從簽出資產 [!DNL Experience Manager] 網頁介面。 如需關於第一種方法的詳細資訊，請參閱 [從Assets UI簽入和簽出檔案](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/managing/check-out-and-submit-assets). 請依照第二個方法的下列步驟，簽出並開啟資產，當 [!DNL Experience Manager] 案頭應用程式已安裝。

1. 開啟 [!DNL Assets] 介面並將指標暫留在資料夾或資產上，以將案頭動作顯示為卡片檢視中的快速動作。

   ![卡片檢視中的屬性選項](assets/desktop_actions_in_card_view.png)

   在選取資產後，或是在資產頁面的工具列中，按一下/點選「案頭動作」圖示，即可使用這些案頭動作。

1. 若要開啟資產，請按一下/點選「在案頭上開啟」快速動作 ![在案頭上開啟圖示](assets/do-not-localize/aemassets_icon_openondesktop.png).

   或者，從工具列的「案頭動作」選單中選擇「開啟」。

   >[!NOTE]
   >
   >當您編輯已開啟但未出庫的檔案時，其他使用者不知道您正在更新資產。

1. 若要開啟要在Adobe Creative Cloud應用程式中編輯的資產，請按一下 ![編輯案頭圖示](assets/do-not-localize/aemassets_icon_editdesktop.png). 此選項也會簽出資產以供編輯。 完成編輯後，將資產入庫以更新中的變更 [!DNL Assets].

   或者，從工具列的「案頭動作」選單中選擇「編輯」。

1. 選取「開啟」功能表選項。 選取的資產會以預覽模式開啟。
1. 若要編輯資產，請選取「編輯」選項。 資產會以編輯模式開啟。

### 從macOS上的Finder檢視資產 {#check-out-assets-on-mac}

應用程式可讓您簽出資產檔案，以防止其他使用者修改您正在處理的檔案。

1. 從Mac內容功能表中，選取「開啟AEM Assets資料夾」選項以開啟「尋找器」。

   ![使用來存取和開啟資產的內容功能表選項 [!DNL Experience Manager] 案頭應用程式](assets/aem_desktopapp_mac_context_menu.png)

   *圖：內容功能表選項，用於存取和開啟使用 [!DNL Experience Manager] 案頭應用程式。*

1. 導覽至您要出庫的資產。
1. 以滑鼠右鍵按一下資產，然後從快顯選單中選取「更多Assets資訊」 。
1. 在「資產資訊」對話方塊中，按一下/點選「簽出」圖示以簽出資產。 在您按一下/點選「簽出」圖示後，「簽入」圖示會切換至「簽入」圖示。

   ![瀏覽至要簽出的資產](assets/browse_assets_to_checkout.png)

1. 若要將資產入庫，使其對其他使用者可用，請按一下/點選「資產資訊」對話方塊中的入庫圖示。

### 在Windows上簽出資產 {#check-out-assets-on-windows}

應用程式可讓您簽出資產檔案，以防止其他使用者修改您正在處理的檔案。

1. 從「內容」選單中，選取「瀏覽Assets」以開啟「總管」。
1. 在Explorer中，導覽至您要出庫的資產位置。
1. 以滑鼠右鍵按一下資產，然後從內容功能表中選取「在網頁上開啟」。
1. 在「資產資訊」對話方塊中，按一下「出庫」圖示。 「出庫」圖示會切換至「入庫」圖示。

   ![簽出圖示可切換](assets/checkout_icon_toggles.png)

1. 在Explorer中檢閱資產。 資產上的鎖定圖示 ![資產鎖定圖示](assets/do-not-localize/aemassets_icon_lockcheckout.png) 表示您已取出資產。

   >[!NOTE]
   >
   >鎖定圖示可能會在一段延遲後出現。 此 [!DNL Experience Manager] 案頭應用程式會快取資產以快速存取，因此可能需要一些時間才能更新鎖定狀態。

1. 若要將資產入庫以供其他使用者使用，請按一下/點選「 」中的「入庫」圖示 **資產資訊** 對話方塊。

### 使用Finder或Explorer並使用網頁介面簽入資產 {#check-in-an-asset-using-finder-or-explorer-and-using-web-interface}

當您完成資產的編輯後，請將這些資產儲存在您的案頭應用程式中。 從內容功能表中，選取 **更多Assets資訊** 並按一下「入庫」。

資產會上傳至 [!DNL Experience Manager] 伺服器。 或者，您可以選取「 」，檢查上傳的狀態 **檢視資產狀態** 從系統匣圖示。 或者，您也可以從以下位置簽入資產： [!DNL Experience Manager] 網頁介面。 按一下已出庫的資產或選取它。 在工具列中按一下入庫圖示 ![簽到圖示](assets/do-not-localize/aemassets_icon_checkin.png).

資產已上傳至 [!DNL Experience Manager] 任何變更儲存在本機後會自動執行。 存回會使其他使用者也能使用該資產 [!DNL Experience Manager] 使用者進行編輯。

### 將資產和資料夾大量上傳至 [!DNL Experience Manager] 伺服器 {#bulkupload}

使用 [!DNL Experience Manager] 案頭應用程式，您可以將包含資產的整個資料夾從您的本機檔案目錄上傳至 [!DNL Assets]. 如此一來，資料夾中的所有資產都會大量上傳，而不需一次上傳一個。

1. 在Assets UI中，按一下/點選 **建立** 在工具列中，然後從功能表中選取 **上傳資料夾**.
1. 瀏覽至您要上傳的資料夾並加以選取。
1. 按一下/點選「確定」。 Assets狀態對話方塊會顯示上傳的狀態。

   ![在「資產狀態」視窗中檢視上傳狀態](assets/aem_desktopapp_bulkupload_status.png)

   在「資產狀態」視窗中檢視上傳的狀態

   >[!NOTE]
   >
   >您可以按一下/點選適當的圖示，手動暫停或取消上傳。

1. 資料夾上傳後，關閉對話方塊並導覽至Assets UI。 上傳的資料夾會顯示在網頁介面中。

Adobe不建議從本機檔案系統複製貼上或拖曳大量檔案或巢狀資料夾至網路共用區域。 由於技術限制和效能不佳，應用程式無法控制上傳程式。

或者，在Finder或Explorer中選取檔案/資料夾、複製檔案/資料夾、瀏覽至網路共用區域中的目標資料夾，然後選擇 **貼上Assets** 從 [!DNL Experience Manager] 案頭應用程式內容功能表。 如此一來， [!DNL Experience Manager] 案頭應用程式開始上傳貼上的資產，類似於以下畫面： **上傳資料夾** 中可用的選項 [!DNL Experience Manager] 網頁介面。

>[!MORELIKETHIS]
>
>* [疑難排解 [!DNL Experience Manager] 案頭應用程式應用程式](troubleshoot-app-v1.md)
