Knowledge workers and end users access HKMaccording to their roles and requirements. Roles determine what data and user interface modules users can access and the actions they can perform. For more information about user roles, see[Product overview](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Getting-started/Product-overview/).

Related topics

[Getting started](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Getting-started/)

## Overview ofHKM interfaces

HKM provides the following interfaces that you can use to manage and share knowledge:

### Knowledge vNext interface

Knowledge vNext ([https://knowledge.HKM.com](https://knowledge.comaround.com)) interface is a web platform for customers that use HKM as a knowledge provider for ITSM and Business Workflows.For more information about configuring HKM as a knowledge provider, see[Leveraging knowledge articles from HKM in other applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Getting-started/Use-cases/Leveraging-knowledge-articles-from-BMC-Helix-Knowledge-Management-by-ComAround-in-other-BMC-applications/).

This interface is designed to provide the best possible experience in knowledge management that is certified for Knowledge Center Services (KCS) v6. It features the familiar style and offers a streamlined user experience. Knowledge workers use this platform daily to create, edit, and maintain knowledge, thus meeting an organization's needs for effective knowledge management.

![vNext_interface.png](.attachments/User-interface-overview_vNext_interface.png)

### HKM Knowledge interface

The HKM Knowledge([zero.comarond.com](http://zero.comarond.com/))interface is a web platform for knowledge workers that includes all the capabilities of HKM.This platform is designed to create, maintain, and share knowledge, as well as to configure your company's administration settings.

### HKM Self-Service interface

The HKM Self-Service([support.HKM.com](http://support.comaround.com/))interface is a web platform for the consumption of knowledge for the end users.The platform is designed to make knowledge articles easy to find and easy to read. It can't be used to create or edit articles.

![Screenshot_ComAround Knowledge interface.JPG](.attachments/User-interface-overview_Screenshot_HKM-Knowledge-interface.JPG)

**![Screenshot_ComAround Self Service interface.JPG](.attachments/User-interface-overview_Screenshot_HKM-Self-Service-interface.JPG)**

Watch the following video to learn more about these interfaces and typical use cases associated with them:

[🎥 Watch Video: https://www.youtube.com/watch?v=E2sFwlPvTro](https://www.youtube.com/watch?v=E2sFwlPvTro)

[![icon-play.png](.attachments/User-interface-overview_icon-play.png)https://youtu.be/E2sFwlPvTro](https://youtu.be/E2sFwlPvTro)

For more information about solutions and components that form HKM architecture, see[HKM architecture](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Getting-started/BMC-Helix-Knowledge-Management-by-ComAround-architecture/).

## Login methods

Knowledge workers and end users can access HKM by using several login methods.

All users are authenticated by using a login server by using the OpenID Connect protocol. Knowledge workers and end users can log in to HKM by using the following methods.

**Important**

To log in to HKM, you must first subscribe to HKM by purchasing the[Service Management Advanced license](https://docs.bmc.com/xwiki/bin/view/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/BMC-Helix-services/BMC-Helix-Service-Management-service/)or the[standalone](https://docs.bmc.com/xwiki/bin/view/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/BMC-Helix-services/BMC-Helix-Knowledge-Management-by-ComAround-service/)license. HKM is also available to customers with entitlements in[Virtual Agent Basic](https://docs.bmc.com/xwiki/bin/view/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/BMC-Helix-services/BMC-Helix-Virtual-Agent-Basic-service/)and[Virtual Agent Advanced](https://docs.bmc.com/xwiki/bin/view/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/BMC-Helix-services/BMC-Helix-Virtual-Agent-Advanced-service/)subscriptions.

| Login method<br> | Description<br> | Example<br> |
| --- | --- | --- |
| HKM<br> | HKM works with Single Sign-On so that knowledge workers do not have to authenticate themselves when they open HKM from ITSM and Business Workflows.<br> | ![test_ITSM.png](.attachments/User-interface-overview_test_ITSM.png)<br> |
| Username and password<br> | Authentication for local users.<br> | ![Login_username and password.png](.attachments/User-interface-overview_Login_username-and-password.png)<br> |
| External Identity Provider (IdP)<br> | Authentication for external users using an external IdP such as Microsoft Entra ID (formerly known as Azure Active Directory (Azure AD).<br> | ![Login_Azure AD.png](.attachments/User-interface-overview_Login_Azure-AD.png)<br> |
| Open portals<br> | Authentication not required for end users.<br> | knowledge.calbro.com<br> |
| Access shared articles<br> | Authentication not required for end users to view the shared articles.<br> | https://zero.HKM.com/link*/16 character GUID*/<br> |

## Permissions to access UI modules in HKM (the HKM Knowledge interface)

The following table describes permissions to access different UI modules for each knowledge worker role:

| **Knowledge worker role**<br> | **UI module inHKM (the HKM Knowledge interface)**<br> | | | | | | |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Content editor - Content section**<br> | **Content editor - Menu settings**<br> | **Content editor - Moving folders**<br> | **Knowledge library**<br> | **Business Intelligence**<br> | **Article Quality Index**<br> | **Administration module**<br> |
| **Candidate**<br> | ❌️<br> | ❌️<br> | ❌️<br> | ❌️<br> | ✅️<br> | ❌️<br> | ❌️<br> |
| **Contributor**<br> | ✅️<br> | ❌️<br> | ❌️<br> | ❌️<br> | ✅️<br> | ❌️<br> | ❌️<br> |
| **Publisher**<br> | ✅️<br> | ❌️<br> | ❌️<br> | ❌️<br> | ✅️<br> | ❌️<br> | ❌️<br> |
| **Coach**<br> | ✅️<br> | ✅️<br> | ✅️<br> | ✅️<br> | ✅️<br> | ✅️<br> | ❌️<br> |
| **Manager**<br> | ✅️<br> | ✅️<br> | ✅️<br> | ✅️<br> | ✅️<br> | ✅️<br> | ✅️<br> |