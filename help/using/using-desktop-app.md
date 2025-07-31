---
title: 使用 [!DNL Experience Manager] 案頭應用程式
description: 使用 [!DNL Adobe Experience Manager] 案頭應用程式。
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 1%

---


# 在案頭上開啟資產 {#openondesktop-v2}

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

按一下資料夾上的&#x200B;**[!UICONTROL Reveal File]**&#x200B;或&#x200B;**[!UICONTROL Reveal Folder]**，以使用本機電腦上預先選取的檔案或資料夾開啟Windows檔案總管或Mac Finder。 例如，在支援放置或連結本機檔案的原生應用程式中放置[!DNL Experience Manager]檔案時，選項很有用。 若要瞭解如何在Adobe InDesign中放置檔案，請參閱[放置圖形](https://helpx.adobe.com/tw/indesign/using/placing-graphics.html)。

**[!UICONTROL Reveal File]**&#x200B;動作會開啟本機網路共用。 它只會顯示本機可用的資產。 也就是說，會顯示使用應用程式揭露、下載或開啟/編輯的資產。 本機網路共用沒有上傳任何變更到[!DNL Experience Manager]。 若要上傳變更，請明確使用應用程式中的&#x200B;**[!UICONTROL Upload Changes]**&#x200B;或&#x200B;**[!UICONTROL Upload]**&#x200B;動作。

>[!NOTE]
>
>為了與[!DNL Experience Manager]案頭應用程式v1.x回溯相容，顯示的檔案是從本機網路共用提供，只會公開本機可用的檔案。 顯示檔案的案頭路徑與應用程式v1.x建立的路徑相同。

>[!CAUTION]
>
>請勿使用&#x200B;**[!UICONTROL Reveal File]**&#x200B;選項編輯原生應用程式中的資產。 請改用&#x200B;**[!UICONTROL Edit]**&#x200B;動作。 若要瞭解更多資訊，請參閱[進階工作流程：共同作業相同的檔案，避免編輯衝突](#adv-workflow-collaborate-avoid-conflicts)。

## 後續步驟 {#next-steps}

* [觀看開始使用Adobe Experience Manager案頭應用程式的影片](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app)

* 使用右側邊欄提供的[!UICONTROL Edit this page] ![編輯頁面](assets/do-not-localize/edit-page.png)或[!UICONTROL Log an issue] ![建立GitHub問題](assets/do-not-localize/github-issue.png)來提供檔案意見回饋

* 聯絡[客戶服務](https://experienceleague.adobe.com/zh-hant?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [瞭解使用者介面](/help/using/user-interface.md)
>* [在案頭應用程式中管理Assets](/help/using/assets-management-tasks.md)
>* [搜尋](/help/using/search.md)
