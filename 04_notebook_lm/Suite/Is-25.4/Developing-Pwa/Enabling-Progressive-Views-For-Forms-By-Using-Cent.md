As a developer, you must enable progress views for out-of-the-box forms and custom forms when creating Progressive Web Applications (PWAs). Use the information in this topic to understand the methods for enabling progressive views for Smart IT and custom applications.

Related topics

[Developing-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/)

[Creating-a-Progressive-View-in-Developer-Studio-to-create-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Creating-a-Progressive-View-in-Developer-Studio-to-create-Progressive-Web-Applications/)

Before you begin

* Make sure that you have installedAR System server, Mid Tier, and Developer Studio.
* If you are a ITSM user, configure a client gateway to access and customize your application by usingDeveloper Studio. For more information, see the following topics in the Subscriber documentation:  
  + [Client Gateway connectivity](https://docs.bmc.com/xwiki/bin/view/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/Getting-started/BMC-Helix-services-lifecycle/Technical-services/Lifecycle-Requests/BMC-Helix-Client-Gateway-connectivity/)
  + [ITSM customizations, configurations, and changes](https://docs.bmc.com/xwiki/bin/view/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/Getting-started/BMC-Helix-ITSM-customizations-configurations-and-changes/)
  + [ITSM Customization policy](https://docs.bmc.com/xwiki/bin/view/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/Policies/BMC-Helix-ITSM-Customization-policy/)
* (Smart ITonly) If you plan to use the**Progressive Views configuration**form, in the Centralized Configuration, make sure that the following parameters are set to the appropriate values:

  | Parameter<br> | Value<br> |
  | --- | --- |
  | **mid\_tier.base.url**<br> | Mid TierURL of Progressive Web Application<br> |
  | **arsystem.security\_iframe\_allowfromurls**<br> | Smart ITbase URL<br> |
  | **Enable-Progressive-Views**<br> | **T**<br> |

  For more information, see[Enabling the Progressive Web Application screens](https://docs.bmc.com/xwiki/bin/view/Service-Management/IT-Service-Management/BMC-Helix-ITSM-Smart-IT/smartit221/Administering/Enabling-the-Progressive-Web-Application-screens/).

## To enable Progressive Views for forms by using the Centralized Configuration Settings

1. In Centralized Configuration, set the**Enable-Progressive-Views**property to**T**(True)as shown in the following image:

   ![enable-pv-in-ccs.PNG](.attachments/Enabling-Progressive-Views-for-forms-by-using-Centralized-Configuration-Settings_enable-pv-in-ccs.PNG)
2. InDeveloper Studio, select the form for which you want to enable progressive views:

   1. From the**Form**menu, select**Create New View**.
   2. From the**View Type**list, select**Progressive.  
      ![PV4.png](.attachments/Enabling-Progressive-Views-for-forms-by-using-Centralized-Configuration-Settings_PV4.png)**

   Developer Studioapplies certain restrictions on modifying progressive views. For more information, see[Customization-best-practices-for-developing-PWA](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Customization-best-practices-for-developing-PWA/).
3. Launch theMid Tierby using the following URL format:  
   ***ARSystemServerName:portNumber*/arsys****/pwa/#/forms/*ARSystemServerName****/formName*/NewDefault%20Administrator%20View  
   For example:  
   **Server1:8080/arsys/pwa/#/forms/Server1/My%20Form/NewDefault%20Administrator%20View**