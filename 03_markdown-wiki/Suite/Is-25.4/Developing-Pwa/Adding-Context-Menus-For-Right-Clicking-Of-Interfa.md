As a developer, you create various objects such as buttons and character fields in a Progressive Web Application (PWA). You might want to enhance the user experience in an application by providing the application users with the option to right-click an object and view a context menu. The context menu provides various options such as opening links in a new tab or a new window.

Related topic

[Creating-a-popup-window-in-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Creating-a-popup-window-in-Progressive-Web-Applications/)

[Adding-rich-text-fields-in-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Adding-rich-text-fields-in-Progressive-Web-Applications/)

Scenario

In Apex Global, Seth the developer wants to provide the application users with the ability to right-click links and view a context menu that displays options such as**Open link in new tab**, and**Open link in new window**. To enable context menus in the application,Seth adds a few properties by using Developer Studio.

Application users see a context menu as shown in the following example illustration:

![Example illustration of a context menu](.attachments/Adding-context-menus-for-right-clicking-of-interface-objects-in-Progressive-Web-Applications_image-2024-3-7_21-57-7.png "Example of a context menu")

You can enable application users to right-click and view a context menu for the following objects:

* Character fields
* Button field with Button Type set to Tertiary
* Table list column fields

## Before you begin

* You must have created a character field, tertiary button, or a table column in Developer Studio.
* You must set the following properties based on the object you create:

  | Object<br> | Property<br> | Value<br> |
  | --- | --- | --- |
  | Character field or character menu  <br> | **Display Type**<br> | **Edit**<br> |
  | **Display > Show URL**<br> | **True**<br> |
  | **Display > Display as text**<br> | **True**<br> |
  | Button<br> | **Button Type**<br> | **Tertiary**<br> |
  | Table column<br> | **Display Type**<br> | **Read Only**<br> |

  **Important**

  These fields must display a non-null value.

## To add context menus for right-clicking the interface objects in Progressive Web Applications

1. Open Developer Studio.
2. Search the form containing the object in which you want to create the link.
3. Open the form.
4. Select the object.  
   The object can be a character field, a tertiary button field, or a table list column field.
5. In the Properties pane, set**Display > HREF Link**to**True**.
6. Set**HREF**to a URL that you want users to open on the PWA screen.  
   Only static URLs are supported.
7. Set**HREF Target**to one of the following options:

   * **Open in the full body of the window**—The destination page occupies the entire browser window.
   * **Open in a new tab**—Opens the link in a new tab.
   * **Open in the same frame**—Opens the link within the iframe view in which the link appears.
   * **Open in the parent frame**—Opens the link in the parent iframe view.
8. Click**Save**.
9. Open the Mid Tier configuration tool and sync the cache.  
   **http://<*MidtierHostName*>:<*PortNumber*>/arsys/shared/config/config\_cache.jsp**

## To test the configuration

1. In a browser, log in to PWA.  
   (*On-premises*)**http://<*midtierHostName*>:<*portNumber*>/arsys/pwa/#/login**(*SaaS*)**http://<*helixBaseURL*>/arsys/pwa/#/login**
2. Change the URL to include the Progressive View form that you created inDeveloper Studio.
3. (*On-premises*)**http://<*midtierHostName*>:<*portNumber*>/arsys/pwa/#/forms/<AR\_Server\_Name>/<formName>/**

   (*SaaS*)**http://<*helixBaseURL*>/arsys/pwa/#/forms/<AR\_Server\_Name>/<formName>/**
4. Confirm that a context menu appears when you right-click the object.  
   You can also open the context menu by using standard keyboard shortcuts of the browser.