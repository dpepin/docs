Even though users are subscribed to HKM and have valid login credentials, they are unable to access help articles within the system.To learn more about product documentation provided by help articles and how to access it, see[Accessing product documentation provided by help articles](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Getting-started/Accessing-product-documentation-provided-by-help-articles/).

Related topics

[Troubleshooting product issues](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Troubleshooting/Troubleshooting-product-issues/)

[Product overview](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Getting-started/Product-overview/)

## Issue symptoms

Users might experience one or more of the following symptoms:

* When attempting to access a help article via a direct link, users receive the following error message:  
  ![page_not_found.png](.attachments/Troubleshooting-access-to-help-articles_page_not_found.png)

* When users search for a help article directly in HKM, no results are found, and the following error message is returned:  
  ![No_search_results.png](.attachments/Troubleshooting-access-to-help-articles_No_search_results.png)

* When users select**Settings**>**Help**in HKM, no help articles are displayed, and the following error message is returned:  
  ![empty_help.png](.attachments/Troubleshooting-access-to-help-articles_empty_help.png)

## Issue causes

Users might be unable to access the help articles for the following reasons:

* The**Help**folder containing the help articles has been deleted from the portal. As a result, users can no longer access the articles.
* The**Help**folder is present in the portal but users do not have the necessary role to access the help articles.

## Resolution for the missing Help folder

HKM provides help articles in the**Help**folder, which is included in the customer portal by default. However, customers have the option to manually delete this folder from the portal. If this folder is removed, all help articles will become unavailable.

To check whether the Help folder is missing and to reinstate it, follow these steps:

Knowledge workers with the following roles can check whether the**Help**folder is missing:

* Contributor
* Publisher
* Coach
* Manager

However, only knowledge workers with the following roles can reinstate the missing**Help**folder:

* Coach
* Manager

Learn more about user roles in[Product overview](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Getting-started/Product-overview/).

1. As a coach or manager, log in to HKM.
2. On the Home page, select**Settings**>**Content editor**.  
   ![settings.png](.attachments/Troubleshooting-access-to-help-articles_settings.png)
3. Expand the folder for your portal and check whether the**Help**folder is present.  
   ![portal.png](.attachments/Troubleshooting-access-to-help-articles_portal.png)
4. If the folder is absent, expand the**Knowledge Library**folder and locate the**Help**folder.  
   ![help_folder.png](.attachments/Troubleshooting-access-to-help-articles_help_folder.png)

   **Important**

   If you expand the**Help**folder, you might not find any help articles. However, these articles are present in the folder, even if they are not visible.
5. Drag and drop the**Help**folder from Knowledge Library to your portal folder, and then click**Subscribe**.  
   ![subscribe.png](.attachments/Troubleshooting-access-to-help-articles_subscribe.png)

After you complete these steps, it may take a few moments for the**Help**folder to appear in your portal. After the folder is added, check to see whether the help articles can be accessed. If the user who experienced the access issue still cannot access the help articles, verify whether the user has the knowledge worker role.

## Resolution for the insufficient role

Only knowledge workers can access help articles. Users with the Reader role cannot view them. As a user, contact your portal manager to verify whether you have the knowledge worker role. Learn more about user roles in[Product overview](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Getting-started/Product-overview/).