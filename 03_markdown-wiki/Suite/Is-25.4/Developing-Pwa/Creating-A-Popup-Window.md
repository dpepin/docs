In a Progressive View, an open popup window looks like an action blade. The popup window does not open in a new window or on a new tab. Instead, it appears as a child window as an action blade by using a docked panel component. The popup window closes automatically when you close the parent window. You cannot move a popup window outside the parent window.

To specify the width of a docked panel:

The blade width is derived from the Width property of the view that you are using in the Open Window action. The following is the behavior:

* (View Width <= 250 AND View Width > 0) = Small = 25% of the whole page
* (View Width > 250 AND View Width <= 500) = Medium = 50% of the whole page
* (View Width > 500 AND View Width <= 750) = Large = 75% of the whole page
* (View Width > 750) = Extra large = 100% of the whole page

The following image shows an open popup window in a desktop view:

![an-open-popup-window-desktop-view.png](.attachments/Creating-a-popup-window-in-Progressive-Web-Applications_an-open-popup-window-desktop-view.png)

The following image shows two open popup windows in a desktop view:

![open-popup-windows-desktop-view.png](.attachments/Creating-a-popup-window-in-Progressive-Web-Applications_open-popup-windows-desktop-view.png)

The following image shows a mobile view, where the action blade occupies full-screen height and width, which is the default behavior of the docked panel component:

![open-popup-window-mobile-view.png](.attachments/Creating-a-popup-window-in-Progressive-Web-Applications_open-popup-window-mobile-view.png)

Related topics

[Developing-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/)

[UI-layout-of-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/UI-layout-of-Progressive-Web-Applications/)