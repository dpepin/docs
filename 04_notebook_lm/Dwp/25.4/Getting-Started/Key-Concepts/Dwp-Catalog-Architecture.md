DWP provides a comprehensive digital employee experience to request services and policies across lines of business such as IT, HR, Facilities, and more. Itprovides administrators with straightforward, highly configurable ways to present the capabilities that end users need to be successful.

Related topics

[DWP-architecture](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Getting-started/Key-concepts/BMC-Helix-Digital-Workplace-architecture/)

[Key-concepts](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Getting-started/Key-concepts/)

[License-types-and-features](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Planning/License-types-and-features/)

The following image shows the architecture ofDWP Catalog:

![DWP C architecture.png](.attachments/DWP-Catalog-architecture_DWP-C-architecture.png)

**Important**

To view the architecture for DWP , see[DWP-architecture](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Getting-started/Key-concepts/BMC-Helix-Digital-Workplace-architecture/).

The following table describes the DWP architecture components:

| Component<br> | Description<br> | Reference<br> |
| --- | --- | --- |
| DWP Catalogconsole<br> | A user interface to configure the service catalog by designing the services and workflows, building reusable questionnaires, managing DWPuser roles, creating promotional banners, and defining entitlements.<br> | [Administering-DWP-Catalog](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Administering/Administering-BMC-Helix-Digital-Workplace-Catalog/)<br> |
| DWP Catalogapplication onIS<br> | An application deployed onISthat includes the record definitions, rules, and associations between the record definitions.<br>Administrators*cannot*modify this application.<br> | Not applicable<br> |
| IS<br> | A no-code platform that helps you to create and automate business processes forDWP Catalog.<br> | Not applicable<br> |
| DWP Catalogconnectors<br> | A method to integrate with other applications such asCMDBandITSM, and specific third-party applications such as Microsoft Office 365 and Active Directory.<br> | [Service-connector-capabilities](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Creating-and-managing-the-service-catalog/Connecting-your-catalog-to-external-systems/Service-connector-capabilities/)<br> |
| Approval inAction Request System<br> | Approvals for specific request types, which end users in DWPcan respond to.<br> | [Enabling-approvals](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Administering/Administering-BMC-Helix-Digital-Workplace/Setting-up-approvals/Enabling-approvals/)<br> |
| CMDBinAction Request System<br> | A capability tosaveDWP Catalogrequests or services as an asset inCMDB.<br> | [Managing-assets-on-floor-maps](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Enabling-self-service-in-an-organization/Locations/Managing-assets-on-floor-maps/)<br> |
| Remote connector framework and third-party service providers<br> | A framework to connect to a remote server that hosts connectors thatDWP Catalogcan use for transferring data to and from third-party service providers via REST calls.<br> | [Integrating-DWP-with-remote-servers](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Developing/Integrating-BMC-Helix-Digital-Workplace-with-remote-servers/)<br> |