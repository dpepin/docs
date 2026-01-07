Check for announcements that might affect future releases of the product or service. These changes can affect the way in which you configure or run your version of HKM.

**Important**

While every effort is made to provide accurate, forward-looking guidance on product direction to assist you with your buying and planning decisions, cannot guarantee that intentions stated as follows are final and binding.

Related topics

[Support information](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Support-information/)

[Release notes and notices](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Release-notes-and-notices/)

## Discontinued features

Discontinued features are no longer available in the product or service.

| Features<br> | Announcements and recommendations<br> |
| --- | --- |
| Screencast-O-Matic<br> | Since November 23, 2023, the Screencast-O-Matic screen recorder has been disabled in HKM.Starting with version 23.3.02, HKM no longer supports the use of this tool. As a result, knowledge workers can no longer use it to make a screen recording in the HKM Knowledge platform.<br>Instead, has introduced a new native video recording tool in the Knowledge vNext platform ([https://knowledge.HKM.com](https://knowledge.comaround.com/)). We recommend that you start using Knowledge vNext to capture the screen when you create or edit articles.<br> |
| Azure Graph APIs<br> | Microsoft has deprecated Azure Active Directory (Azure AD) Graph as of June 30, 2023, and moved it into the retirement phase. HKM has used Azure AD Graph APIs to integrate its login server with Microsoft Entra ID (formerly known as Azure Active Directory (Azure AD).<br>Starting with version 23.3.02, HKM will use Microsoft Graph API to integrate the login server with Microsoft Entra ID.<br>All affected customers have already been notified of this change.<br> |
| Customer types<br> | Starting with version 23.3.02, HKM no longer supports the following customer types:<br>  * Legacy * Team  All Legacy and Team customers will be upgraded to the Professional customer type.<br> |
| Azure Media Services<br> | Microsoft has announced the retirement of Azure Media Services on 30 June 2024, after which it will no longer be supported. HKM has used Azure Media Services to encode uploaded videos.<br>Therefore, starting with version 23.3.02, HKM will no longer use Azure Media Services to encode uploaded videos. As a result, users can upload videos only with the MP4, WebM, and OGG extensions, and these videos must be in an HTML-supported format.<br> |
| Visits report<br> | Starting with version 23.3, HKM no longer supports generating the Visits report for analyzing new data. Due to the changes in Azure Application Insights data streaming, HKM stops tracking page views in the application. As a result, the Visits report is no longer populated with new data and will be removed from the application in the near future. Currently, you can continue using it for analyzing historical data that was collected prior to the release of version 23.3. However, if you select a time period for displaying data after the release of version 23.3, you see a blank report.<br>![visits_report.png](.attachments/Deprecated-and-discontinued-features_visits_report.png)<br> |
| Multi-import of a single Microsoft Word document (.docx)<br> | Starting with version 22.1.05, HKM no longer supports creatingmultiple articles and folders from a single Microsoft Word (.docx) document imported to HKM.<br> |
| Drag-and-drop sorting for lists<br> | * Starting withversion 22.1.05, HKM no longer supports drag-and-drop sorting of articles and folders in menu lists and the content tree. **Important:**This feature is discontinued for all knowledge portals.  * Starting withversion 22.1.05, article and folder lists are sorted alphabetically, and you can no longer manually control the order of items. If a list contains both articles and folders, the folders have a higher priority and are displayed first. However, you can still manually arrange the order of items for the following UI sections and widgets:   + Folders on the top menu bar   + Recommended widget   + News widget |
| eLearning<br> | Starting with version 22.1.05, HKM no longer supports the use of the eLearning feature.<br>Note howHKM has handled the existing eLearning content created before the 22.1.05 release:<br>  * All eLearning folders have been converted to standard folders. * The eLearning overview page has been converted to the standard search results page. * All eLearning links are redirected to the search results page. |
| Period of validity<br> | Starting with version 22.1.05, HKM no longer supports setting a validity period for knowledge articles.<br>has replaced this feature with the Knowledge state scheduler functionality. We recommend that you start using the Knowledge state scheduler to plan and schedulethe automatic change of your article's knowledge state on a specific date.<br> |