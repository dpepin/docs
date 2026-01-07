announces that the Jira connector provided with theDWP Catalogwill be discontinued.

**Important**

While every effort is made to provide accurate, forward-looking guidance on product direction to assist you with your buying and planning decisions, cannot guarantee that the intentions stated as follows are final and binding.

Related topics

[Support-information](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Troubleshooting/Support-information/)

[Release-notes-and-notices](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Release-notes-and-notices/)

[Deprecated-and-discontinued-features](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Release-notes-and-notices/Deprecated-and-discontinued-features/)

## Background

DWP Catalogprovides the Jira connector to create a Jira ticket that corresponds to a catalog service request. In the Catalog workflow, you use the**Create Jira issue**to populate the required fields in Jira.

## Statement of direction

ends support for the Jira connector provided with theDWP Catalog. recommends that you use iPaaS, powered by Jitterbit, to integrate with Jira. Use one of the following templates:

* **Create Jira Issue from DWP Request**template to create a Jira issue and synchronize attachments and comments. For more information, see[Creating Jira issues from DWP requests by using Jitterbit Harmony](https://docs.bmc.com/xwiki/bin/view/Helix-Common-Services/iPaaS/BMC-Helix-iPaaS/bhip2002/BMC-Helix-iPaaS-powered-by-Jitterbit/Integrating-by-using-integration-templates-powered-by-Jitterbit/Creating-Jira-issues-from-BMC-Helix-Digital-Workplace-requests-by-using-Jitterbit-Harmony/).
* **Create Jira issues from DWP requests by using MuleSoft Anypoint Platform**template to create a Jira issue, synchronize attachments and comments, and update the service request status to Closed when the Jira issueis resolved.For more information, see[Creating Jira issues from DWP requests by using MuleSoft Anypoint Platform](https://docs.bmc.com/xwiki/bin/view/Helix-Common-Services/iPaaS/BMC-Helix-iPaaS/bhip2002/BMC-Helix-iPaaS-powered-by-MuleSoft/Integrating-by-using-integration-templates-powered-by-MuleSoft/Creating-Jira-issues-from-BMC-Helix-Digital-Workplace-requests-by-using-MuleSoft-Anypoint-Platform/).