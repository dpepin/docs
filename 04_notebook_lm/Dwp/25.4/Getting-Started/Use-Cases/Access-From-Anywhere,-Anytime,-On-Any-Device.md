Employees can access DWP on their preferred devices from any location at any time. They can easily request services and access information through various channels, including web browsers, Slack, SMS, Microsoft Teams, orVirtual Agent. The application is designed to be accessible across multiple devices, including desktops, tablets, and mobile devices, ensuring a consistent user experience regardless of the location and the communication channel.

Related topics

[Using-DWP-to-request-services](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Using-BMC-Helix-Digital-Workplace-to-request-services/)

![Access BMC Helix Digital Workplace anywhere, anytime, on any device](.attachments/Access-from-anywhere%2C-anytime%2C-on-any-device_access_anywhere.png "Access BMC Helix Digital Workplace anywhere, anytime, on any device")

The benefits include:

* Enhanced mobility and accessibility**:**Accessing from any place or device gives users with mobility and accessibility, ensuring a constant connection to DWP.
* Device independence: Users can seamlessly access the application across a range of devices, including laptops, smartphones, and tablets.
* Location independence: Users can connect to the application from any location, whether in the office, at home, or on the go.
* Multi-channel support: The application is available through various channels, such as email, phone, chat, and self-service portals, allowing users to effortlessly switch between them. Users have an uninterrupted connection with the application, even when transitioning between communication channels.
* Enhanced supportability: Users can seamlessly switch between channels without losing the context of their interaction. They can converse withVirtual Agentwithin the application and effortlessly transition from a bot to a live agent for enhanced support.

Scenario 1: Omnichannel engagement

Scenario

Before a campaign launch, Britney, the marketing manager, realizes that the analytics tool is not functioning correctly. She consults with HelixGPT inDWPfor help; however, the suggestions do not fulfill her needs. HelixGPT offers her the option to chat with a live agent or raise a request. She submits a service request and simultaneously escalates the issue through the chatbot. The IT team quickly acknowledges her request, provides a potential workaround and resolves the issue. Britney interacted seamlessly with IT support through various integrated channels.

## Scenario 2:Road warrior

Scenario

Joe is travelling for the first time to the Boston office. At the airport, he wonders if his employee badge will work there. Joe opensDWPon his mobile phone. After consulting with HelixGPT, he is given the option to submit a request to get access to the office added to his existing card, which he accepts. In Boston, Joe receives a notification that his request has been resolved. At the office, he swipes his badge and lets himself in.

## Scenario 3:Self-service from WhatsApp

The following scenario applies to![DWP Advanced icon.png](.attachments/Access-from-anywhere%2C-anytime%2C-on-any-device_DWP-Advanced-icon.png)[DWP](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Planning/License-types-and-features/).

Scenario

Mary spends much of her day on WhatsApp, responding to queries from the team she supports. She needs WiFi access for a visiting customer, so she consults HelixGPT on WhatsApp and says, "Request guest WiFi." She answers a few questions and soon gets credentials she can give the visiting customer. That evening,Mary has problems connecting to the VPN from home. She again consults HelixGPT on WhatsApp and says, "Cannot connect to VPN." HelixGPT generates an answer and proposes self-help resolution steps based on knowledge articles in the knowledge base. She follows the steps and connects to the VPN.

## Access from any device

As an administrator, you can make DWP available to your users via desktop and mobile devices (Apple iOS and Google Android). On mobile devices, you can access DWP by using the same URL you use on the web. Neither Android nor iOS mobile devices require any special app.

However, iOS users have to download the iOS wrapper app from the Apple App Store to use push notifications and QR code scans.The minimum iOS version required for DWP is iOS 15. This requirement applies to installing the wrapper app and accessing the application via the mobile browser. You can also distribute the wrapper app to iOS devices within your organization through your Mobile Device Management (MDM) solution. You require the following MDM keys stored in the user default settings:

* com..configuration.managed.myit-server
* com..configuration.managed.myit-port

![Make BMC Helix Digital Workplace available to users on all devices](.attachments/Access-from-anywhere%2C-anytime%2C-on-any-device_Omni-channel_with_MDM.png "Make BMC Helix Digital Workplace available to users on all devices")

The process described in[Rebranding-DWP](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Administering/Administering-BMC-Helix-Digital-Workplace/Customizing-and-rebranding-the-BMC-Helix-Digital-Workplace-user-interface/Rebranding-BMC-Helix-Digital-Workplace/)applies the branding changes to all desktop and mobile users. Remember that the Apple iOS wrapper app or its name cannot be rebranded on iOS devices. However, you can rebrand the app's content by using the rebranding functionality in the Admin console. This rebranding will appear the same on iOS devices as it does on Android devices and desktop web browsers.

You need to configureVirtual Agentor a chatbot forDWP to enable interaction over various user communication channels such as Slack, Microsoft Teams, SMS, and WhatsApp.For more information, see[Integrating-DWP-Catalog-with-Virtual-Agent](https://docs.bmc.com/xwiki/bin/create/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Integrating/Integrating-BMC-Helix-Digital-Workplace-Catalog-with-BMC-Helix-Virtual-Agent/WebHome?parent=Service-Management.Employee-Digital-Workplace.BMC-Helix-Digital-Workplace.dwp254.Getting-started.Use-cases.Access-from-anywhere-anytime-on-any-device.WebHome). See also[Configuring a chatbot to work with a communication channel](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Virtual-Agent/hva251/Administering/Configuring-BMC-Helix-Virtual-Agent-with-IBM-Watson-Assistant/Configuring-a-chatbot-to-work-with-a-communication-channel/).