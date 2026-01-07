As a developer, you can create panes that application users can resize according to their preferences.When you add resizable panes, users can expand the panes that have large amounts of information, thereby improving readability and user experience.

Related topic

[Flow-panel-holders-for-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Flow-panel-holders-for-Progressive-Web-Applications/)

[Panel-holder-display-types-in-Progressive-View](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Panel-holder-display-types-in-Progressive-View/)

Scenario

At Apex Global Inc., the change request screen has an activity pane where the volume of content is sometimes large.Due to the fixed width of the activity pane, users need to scroll the pane to view all the content. Making the pane width adjustable could improve the user experience.

To enable users to resize the activity pane, the developer Seth creates a resizable pane by using Developer Studio. Users can increase the width of the activity pane when they want to view more content.

The following animation shows an example of a resizable pane displayed on a PWA screen:  
![202403041432-resizable pane anim.gif](.attachments/Creating-resizable-panes-in-Progressive-Web-Applications_202403041432-resizable-pane-anim.gif)

## To create resizable panes in Progressive Web Applications

1. In Developer Studio, create a progressive view.  
   1. Select**Form > Create New View**.  
      The Create New View dialog box is displayed.
   2. From the**View Type**list, select**Progressive**.  
      ![Create New View dialog box](.attachments/Creating-resizable-panes-in-Progressive-Web-Applications_Create-new-view.png "Create New View dialog box")  
      Developer Studioautomatically creates a section panel.
2. From the Palette pane, drag a Splitter Panel Holder into the view.  
   ![image-2024-3-4_16-29-59.png](.attachments/Creating-resizable-panes-in-Progressive-Web-Applications_image-2024-3-4_16-29-59.png)
3. Set a value for the property**Display > Splitter Min Width Percent**.  
   This is the minimum width to which users can resize the pane.

   The Default value of**Splitter Min Width Percent**is**20**.
4. Click**Save**.
5. Open the Mid Tier configuration tool and sync the cache.  
   **http://<*MidtierHostName*>:<*PortNumber*>/arsys/shared/config/config\_cache.jsp**

To test and review the resizable panes in Progressive Web Applications

1. In a browser, log in to PWA.  
   (*On-premises*)**http://<*midtierHostName*>:<*portNumber*>/arsys/pwa/#/login**(*SaaS*)**http://<*helixBaseURL*>/arsys/pwa/#/login**
2. Change the URL to include the Progressive View form that you created in Developer Studio.  
   (*On-premises*)**http://<*midtierHostName*>:<*portNumber*>/arsys/pwa/#/forms/<AR\_Server\_Name>/<formName>/**(*SaaS*)**http://<*helixBaseURL*>/arsys/pwa/#/forms/<AR\_Server\_Name>/<formName>/**
3. Confirm whether the resizable pane can be set to the minimum width.  
   The width of the pane you set is saved across sessions, that is, when you log in again, you will see the previously set width of the pane.