---
title: '[!DNL Adobe Experience Manager]案頭應用程式發行說明'
description: ' [!DNL Adobe Experience Manager] 案頭應用程式的發行詳細資料、增強功能、新功能、相容性和下載連結。'
mini-toc-levels: 1
feature: Desktop App,Release Information
exl-id: e058e7a2-fcc8-4ad1-899e-20695db6bc72
source-git-commit: b1fad118e1ffbd0809afe9a33bcb848648cd8bdd
workflow-type: tm+mt
source-wordcount: '2470'
ht-degree: 9%

---

# [!DNL Adobe Experience Manager]案頭應用程式發行說明 {#release-notes-v2}

最新案頭應用程式3.0.0版的發行資訊如下。 發行日期為2025年7月31日。

最新版本的案頭應用程式包含下列錯誤修正和增強功能：

* 您可以從本機電腦將新建立的資產上傳到AEM （儲存中央存放庫），然後在您的案頭應用程式中檢視這些資產。
* 自動重新整理功能會自動即時更新內容，確保您一律看到最新資訊，不會手動重新載入頁面及取得已更新資產的清單。
* 釘選或取消釘選資料夾功能可讓您釘選重要資料夾，或是在不再需要重要資料夾時取消釘選以取消釘選檢視，讓這些資料夾保持可存取性。
* 重新命名標題功能可讓您輕鬆更新或修改資產的標題，協助您隨著內容發展保持名稱正確且井然有序。
* 您可以保留原始檔案，並使用複製檔案作業在本機和雲端位置之間複製檔案，以變更類似檔案。
* 簽入和簽出功能可讓您鎖定檔案進行編輯（簽出）並儲存您的變更，同時讓其他人可以使用此檔案（簽入），以管理檔案存取。
* 您可以檢視、下載和瀏覽集合。
* 您可以在建立新資料夾時指派中繼資料。
* Experience Manager案頭應用程式現在可讓您將資產或資料夾移動至新位置，同時保留其中繼資料，協助組織和簡化檔案系統。
* 新增對下載收藏集中可用資料夾的支援。
* 匯出選項現在允許從案頭應用程式下載選取的檔案和資料夾，以平面結構下載到它們的特定目標位置。
* Desktop App現在會自動識別在本機檔案系統上已下載資料夾中建立的新檔案，並將其上傳至AEM。 案頭應用程式必須保持開啟狀態，才能識別本機檔案系統上的新檔案。
* 自動同步功能現在可讓收藏集中的下載資產定期將AEM資產管理與本機檔案系統同步。
* AEM Desktop App現在可讓您檢視資料夾屬性，例如資料夾縮圖、大小、路徑、建立日期、標籤、中繼資料等。
* 您現在可以存取卡片檢視、格線檢視或樹狀檢視中的資產，以乾淨、整齊且美觀的資產版面配置。
* 將資產從案頭應用程式拖曳至目標Creative Cloud應用程式的功能。 案頭應用程式會自動簽出資產並將其下載到本機檔案系統。
* 當您更新屬於集合一部分的資產時，系統會自動在暫存快取資料夾和案頭應用程式UI中更新該資產。
* UI上會更新各種選項的各種標籤，讓應用程式更直覺。

**支援的[!DNL Experience Manager]版本**&#x200B;為：

* [!DNL Experience Manager]作為[!DNL Cloud Service]。 請參閱[發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/release-notes/home)。
* [!DNL Experience Manager] 6.5.0或更新版本，在Adobe Managed Services (AMS)或內部部署上。 請參閱[Service Pack發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-65/content/release-notes/release-notes)。

[!DNL Adobe Experience Manager]案頭應用程式可用於下列&#x200B;**作業系統**：

* macOS X 10.14或更新版本，提供最新的錯誤修正。
* Windows 10搭配最新的Service Pack與錯誤修正。

AEM案頭應用程式2.3.1版及更新版本提供兩個版本的Windows安裝程式。 基礎安裝程式會將AEM案頭應用程式安裝在使用者的本機「應用程式資料」目錄下。 Adobe建議大部分使用者使用此安裝程式。 也可以使用Enterprise Windows安裝程式，將AEM案頭應用程式安裝在共用程式檔案目錄下。 這兩種安裝程式會安裝相同版本的AEM案頭應用程式，且功能上沒有任何差異。

支援作業系統的&#x200B;**下載URL**&#x200B;為：

| 作業系統 | [!DNL Experience Manager] as a [!DNL Cloud Service] | [!DNL Experience Manager] 6.x |
|---|---|---|
| macOS (v3.0.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-3.0.0.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-3.0.0.dmg) |
| macOS Apple Silicon (M1) (v3.0.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-3.0.0.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-3.0.0.dmg) |
| Windows 64位元(v3.0.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-3.0.0.exe) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-3.0.0.exe) |
| Windows 64位元Enterprise (v3.0.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-ent-3.0.0.msi) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-ent-3.0.0.msi) |
| macOS (v2.3.3) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.3.3.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.3.3.dmg) |
| macOS Apple Silicon (M1) (v2.3.3) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.3.3.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.3.3.dmg) |
| Windows 64位元(v2.3.3) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.3.3.exe) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.3.3.exe) |
| Windows 64位元Enterprise (v2.3.3) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.3.3.msi) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.3.3.msi) |
| macOS (v2.3.1) | [下載連結](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-osx-x64-2.3.1.dmg&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081954149%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=mwSX5ilZL0he2raIx8t5ecQ%2FWuizky4MpcCXX3mEN38%3D&reserved=0) | [下載連結](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-osx-x64-2.3.1.dmg&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081981239%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=LJH3OCFq7yRykN4wU8HN9%2FBXC%2BjfXLJH4QizeFZfRHE%3D&reserved=0) |
| macOS Apple Silicon (M1) (v2.3.1) | [下載連結](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-osx-arm64-2.3.1.dmg&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081965822%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=2YENn0tDduiucogClt6aBZHDOE6dbzBdigq8VQawIO0%3D&reserved=0) | [下載連結](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-osx-arm64-2.3.1.dmg&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081986151%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=jCepldg4dMej0%2BrK2mUonXwqsWL8ksE8%2BLMSgsH9qTA%3D&reserved=0) |
| Windows 64位元(v2.3.1) | [下載連結](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.exe&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081970892%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=sRn2UWW%2Bi7SMEvSO74ZGGvJ40vHh1KhLc7zAfKc37Es%3D&reserved=0) | [下載連結](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.exe&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081991004%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=aQWZtEK%2F3cWX8n8Au%2FwZ5Zd9xPVo5phvk%2FuF%2Be0HRrE%3D&reserved=0) |
| Windows 64位元Enterprise (v2.3.1) | [下載連結](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.msi&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081976350%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=v9C0sLDSkuL%2FMIyae2WkbitJPVgSlAw2BqcaH5Im0uw%3D&reserved=0) | [下載連結](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.msi&data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081995827%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&sdata=2btCh0aIrUBiyeG37K9YorvzTeIJOggbq%2FRauUMn4LY%3D&reserved=0) |
| macOS (v2.3.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) |
| macOS Apple Silicon (M1) (v2.3.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) |
| Windows 64位元(v2.3.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) |
| macOS (v2.2.2) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) |
| macOS Apple Silicon (M1) (v2.2.2) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) |
| Windows 64位元(v2.2.2) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) |
| macOS (v2.2.1) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) |
| macOS Apple Silicon (M1) (v2.2.1) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) |
| Windows 64位元(v2.2.1) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) |
| macOS (v2.2.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) |
| macOS Apple Silicon (M1) (v2.2.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) |
| Windows 64位元(v2.2.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) |
| macOS (v2.1.5.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) |
| Windows 64位元(v2.1.5.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) |
| Windows 32位元(v2.1.5.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) |
| macOS (v2.1.4.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) |
| Windows 64位元(v2.1.4.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) |
| Windows 32位元(v2.1.4.0) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) |
| macOS (v2.1.3.4) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) |
| Windows 64位元(v2.1.3.4) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) |
| Windows 32位元(v2.1.3.1) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) | [下載連結](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) |

## 支援不同的資產和檔案型別 {#support-for-file-types}

應用程式支援儲存在[!DNL Experience Manager]中的資產，這些資產代表二進位檔案以進行其基本作業。 在原生桌面應用程式中開啟檔案時，需透過作業系統內的特定應用程式（例如 Mac Preview 或 Adobe Photoshop），以特定檔案類型（例如 PNG 或 JPG）開啟。

部分檔案類型支援將連結的資產放入二進位檔。使用案頭應用程式開啟此類二進位檔案時，若資產存在於[!DNL Experience Manager]存放庫中，應用程式會預先下載連結的資產。 目前支援的檔案類型包括：

* [!DNL Adobe InDesign]個檔案（INDD格式）
* [!DNL Adobe Illustrator]個檔案（AI格式）
* [!DNL Adobe Photoshop]個檔案（PS格式）

上述應用程式的[!DNL Adobe Creative Cloud] 2018和[!DNL Adobe Creative Cloud] 2019版本支援此功能。 應用程式會使用啟發式、最佳比對方法，將連結資產的本機案頭路徑對應至[!DNL Experience Manager]伺服器上的URL。 依賴的假設如下：

* 原生應用程式中置入檔案的路徑使用全域案頭路徑（從顯示有[!UICONTROL Reveal]選項的本機網路共用置入）。

* 原生應用程式會將路徑儲存在檔案的XMP記錄中。

* [!DNL Experience Manager]已擷取XMP記錄，其中包含資產中繼資料記錄的路徑。

* 路徑與[!DNL Experience Manager]中的資產相符，也就是說，置入的檔案也位於相符路徑下的[!DNL Experience Manager]中。

## 新功能、增強功能和錯誤修正 {#what-is-new}

若要瞭解詳細資訊，請參閱[v2.0](introduction.md#whats-new-v2)的新增功能。

**應用程式v2.3.1**&#x200B;中的更新

* 新的Enterprise Windows Installer會在「程式檔」下安裝應用程式。
* 在AEM和SSO登入期間支援&#x200B;**基本驗證**。
* 上傳作業期間允許的可設定資產數量

**應用程式v2.3.0**&#x200B;中的更新

* 新增IMS登入支援。 IMS整合可讓案頭應用程式自動執行存取權杖重新整理，讓使用者最多可保持登入14天。

* 改善對公司代理和網頁篩選的支援。

**應用程式v2.2.2**&#x200B;中的更新

* （僅限Windows）安裝2.2.0和2.2.1發行版本後，案頭應用程式會顯示空白熒幕。

**應用程式v2.2.1**&#x200B;中的更新

* 按一下&#x200B;**[!UICONTROL Sign In]**&#x200B;時，案頭應用程式會顯示工作階段逾時錯誤訊息。

* 在macOS上存取案頭應用程式v2.2.0時發生問題。

* 按一下&#x200B;**[!UICONTROL Edited Locally]**&#x200B;排序資產時，案頭應用程式會顯示錯誤訊息。

**應用程式v2.2.0**&#x200B;中的更新

* 支援Apple矽(M1)。

* 能夠記憶登入案頭應用程式時的連線字串。

**應用程式v2.1.5.0**&#x200B;中的更新

* 當您上傳包含中文字元的資料夾中的檔案時，案頭應用程式會停止回應(ASSETS-9237)。

* 案頭應用程式以檔案名稱中的破折號取代點(ASSETS-10955)。

**應用程式v2.1.4.0**&#x200B;中的更新

新版應用程式提供錯誤修正。

**應用程式v2.1.3.4**&#x200B;中的更新

新版應用程式提供錯誤修正。

**應用程式v2.1.3.3**&#x200B;中的更新

新版應用程式提供錯誤修正。

**應用程式v2.1.3.2**&#x200B;中的更新

此版本的應用程式提供錯誤修正。

**應用程式v2.1.3.1**&#x200B;中的更新

此版本修正的錯誤為：

* 即使使用大型資產，資產上傳和下載速度也有所改善。 此版本修正上傳非常大的檔案時，資產透過[!DNL desktop app]上傳有時失敗的問題。

**應用程式更新v2.1.2.0**

* [!UICONTROL Clear Cookies]的新選項已新增至應用程式的主功能表。 它有助於解決可能的登入問題，例如將伺服器連線變更為另一個伺服器時。 在連線前先檢視[清除Cookie](/help/using/troubleshoot.md#cannot-login-cookies-issue)。

* 已新增一個選項，如果選取，可讓應用程式上傳在[!DNL Adobe Experience Manager]中節點名稱符合本機檔案和檔案夾名稱的檔案夾和檔案。 此程式可確保本機名稱與上傳名稱之間的一致性。

  此行為類似於案頭應用程式版本1中的預設行為。 而在目前版本中，如果未啟用選項，則資料夾名稱中的空格和字元`% ; # , + ? ^ { } "`會取代為資料夾路徑中的破折號。 此外，資料夾路徑中的大寫字元會轉換為小寫。 不過，在檔案名稱中，字元`# % { } ? &`會以破折號取代；但會保留空格與大小寫。 如需詳細資訊，請參閱[應用程式偏好設定](/help/using/install-upgrade.md#set-preferences)和[上傳並新增資產](/help/using/upload-assets.md#upload-and-add-new-assets-to-aem)。

**應用程式更新v2.1.1.0**

* 進階設定可讓應用程式在上傳資料夾時模擬v1.10應用程式行為。 在v1.10中，在存放庫中建立的節點名稱會遵循使用者提供的資料夾名稱空格和大小寫。 在2.1版中，預設行為未變更：資料夾名稱中的多個空格會由存放庫節點名稱中的連字型大小取代，而節點名稱會轉換為小寫。 檢視[應用程式偏好設定](/help/using/install-upgrade.md#set-preferences)。

**應用程式更新v2.1.0.0**

* 若要上傳資產，使用者現在可以直接從Windows檔案總管或Mac Finder在應用程式的介面上拖曳檔案或資料夾。 除了應用程式中可用的上傳選項外，此程式也可運作。 檢視[上傳資產](/help/using/upload-assets.md#upload-and-add-new-assets-to-aem) <!-- CQ-4309527 -->

**應用程式更新v2.0.3**

此版本修正的錯誤為：

* 修正Windows上嘗試存取[!DNL Adobe Experience Manager] 6.5.5.0上DAM存放庫的應用程式使用者登入問題。

**應用程式v2.0.2**&#x200B;中的更新

錯誤修正和更新包括：

* 現在提供上傳加速設定以提高上傳效能。 開啟此設定時，應用程式會使用更多本機CPU執行緒，以更快的速度上傳，且耗用更多資源。

* 若檔案名稱或路徑包含特定GB18030字元已固定，則會上傳資產。<!-- CQ-4283494 -->

* 在搜尋結果中切換為其他排序型別後，即可使用依關聯性排序選項。<!-- CQ-4286874 -->

* 案頭應用程式現在會列出子資料夾，不需要明確重新整理。<!-- CQ-4285711 -->

* (Windows)修正某些Windows電腦無法使用應用程式介面的罕見問題。 使用者無法點選應用程式介面，因為介面元素的點選區域向側邊偏移，導致介面看起來扭曲。<!-- CQ-4280785 -->

**應用程式v2.0.1**&#x200B;中的更新

錯誤修正和更新包括：

* 允許選項設定`%Temp%`目錄以符合`%APPDATA%`路徑。<!-- CQ-4282665 -->

* 允許使用者透過Okta SAML驗證登入[!DNL Experience Manager]作者。<!-- CQ-4278134 -->

## 安裝指示 {#installation-instructions-v2}

若要瞭解如何安裝和設定應用程式，請參閱[安裝 [!DNL Experience Manager] 案頭應用程式](install-upgrade.md)。

如果您要從舊版[!DNL Experience Manager]案頭應用程式進行升級，您必須遵循列於[從舊版](install-upgrade.md#upgrade-from-previous-version)進行升級的最佳作法進行轉換。

## 應用程式運作方式的重要附註 {#how-app-works}

請務必瞭解以下關於應用程式及其運作方式的資訊。

* 應用程式可完整控制需要從[!DNL Experience Manager]到完整傳輸資產二進位檔的作業(**開啟**、**編輯**、**上傳變更**&#x200B;和&#x200B;**上傳Assets**)。

   * 如果想要在案頭使用資產，您必須明確地「開啟」、「編輯」或「下載」資產至案頭，並可使用個別檔案、資料夾或多個檔案選取的方式進行上述操作。

   * 若要將資產的本機變更內容上傳至[!DNL Experience Manager]，您必須個別或透過多重選取方式選取[!UICONTROL Upload Changes]。

   * 應用程式不是將資產同步到案頭與[!DNL Experience Manager]上的「同步使用者端」。

   * 應用程式未提供將[!DNL Experience Manager]存放庫對應為虛擬資料夾結構的網路共用。

* 應用程式顯示的資產清單是根據Assets存放庫的狀態。 應用程式不會顯示或管理從本機下載、隨後在本地檔案或快取資料夾中重新命名的檔案。

* 如果應用程式未顯示預期的結果，請按一下頂端列中的重新整理圖示。

* 區域網路共享（在您進行 [!UICONTROL Reveal File] 動作時顯示）只會顯示本機可用的檔案（和資料夾）。[!UICONTROL Reveal File] 和 [!UICONTROL Reveal Folder] 會預先下載資產，協助您取得顯示在區域網路共享中的正確資產。

* 當Adobe Creative Cloud應用程式讀取連結/置於Creative Cloud應用程式原生檔案中的資產檔案時，會使用SMB (Mac) / WebDAV (Win)本機網路共用。

下圖說明資產和檔案如何從雲端移動至本機檔案系統（反之亦然），這是由使用者動作所啟動。

![透過案頭應用程式，資產從[!DNL Experience Manager]伺服器流向原生案頭應用程式](assets/da20_flow_diagram.png)

## 已知問題 {#known-issues-v2}

**使用者介面問題：**

* 某些時候，案頭應用程式的介面可能會變成空白。 按一下滑鼠右鍵並按一下[!UICONTROL Refresh]以重新載入應用程式。 在重新整理後，您會從DAM存放庫的根目錄開始。 資產的更新或狀態會保留。<!-- CQ-4270267 -->

* 在沒有軌跡板或滑鼠指標的情況下，很難導覽資料夾/搜尋結果。 沒有滾輪的滑鼠裝置不會顯示卷軸。<!-- CQ-4269947 -->

* 少數情況下，當上傳的資產變更時，進度列可能無法顯示正確的進度。

* 在您套用、移除篩選器以尋找所有在本機編輯的資產後，應用程式不會將使用者引導至剛開始的搜尋結果或資料夾檢視。應用程式會顯示 DAM 資料庫的根資料夾。

* 某些時候，當您連線至未執行[!DNL Experience Manager]伺服器的URL時，連線畫面會停止回應。 請退出應用程式並重新啟動。

**CRUD（建立、讀取、更新和刪除）相關問題：**

* 當上傳含有註解的變更至資產時，註解會與資產一併儲存在[!DNL Experience Manager]中，但無法顯示為版本設定註解。 此問題已在[!DNL Experience Manager] 6.4.5和[!DNL Experience Manager] 6.5.1中解決。Adobe建議您安裝最新的Service Pack。<!-- CQ-4268990 -->

* 使用者無法取消資產傳輸。 如果您不小心觸發了非預期的大量傳輸，請退出應用程式並重新啟動。<!-- CQ-4278940 -->

**平台問題：**

* 某些時候，即使您可能尚未編輯資產，Windows 上的資產狀態可能會在開啟後立即變更為 [!UICONTROL Edited Locally]。按一下 [!UICONTROL Refresh] 以更新。

>[!MORELIKETHIS]
>
>* [[!DNL Experience Manager] 作為 [!DNL Cloud Service] 檔案](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service)
>* [[!DNL Experience Manager] 作為 [!DNL Cloud Service] [!DNL Assets]檔案](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/assets/overview)
>* [如何使用 [!DNL Experience Manager] 案頭應用程式](using-desktop-app.md)
>* [安裝和升級桌面應用程式](install-upgrade.md)
>* [最佳作法與疑難排解提示](troubleshoot.md)
