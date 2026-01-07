When panels on application screens have different quantities of content, a normal scroll bar creates blank spaces in the panels that have less content. A sticky panel helps avoid such blank spaces by scrolling the panel with more content at a different rate.

You can add sticky panels in Progressive Web Applications (PWA) screens with multiple panels by usingDeveloper Studio. Adding sticky panels helps improve user experience when your users scroll screens with multiple panels displaying different amounts of content.

Sticky panels scroll in such a way that the panel with more content scrolls first so that scrolling of all the panels completes at the same time. Application users can see the content of the panels easily, without any of the content going out of view.

Scenario

At Apex Global, the change request screen has an activity panel which often has more scrollable content than the main panel. When users scroll down to view the activity panel content, the content in the main panel goes out of view.

The following animation shows a scenario where the panel on the left scrolls out of view leaving an empty space:

To address this issue, the application developer, Seth, adds a property in Developer Studiothat causes both the panels to scroll at different rates based on their content. The panel with more content scrolls first while the panel with less content remains sticky, until both panels have the same amount of scrollable content.

The following animation shows how a sticky panel behaves when scrolling:

Related topics

[Panel-holder-display-types-in-Progressive-View](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Panel-holder-display-types-in-Progressive-View/)

[Flow-panel-holders-for-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Flow-panel-holders-for-Progressive-Web-Applications/)

[Navigation-fields](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-applications-by-using-Developer-Studio/Developing-the-application-interface/Creating-and-managing-fields/Navigation-fields/)

## Before you begin

You must start with an existing form that has more than one panel with the following properties:

| Property<br> | Value<br> |
| --- | --- |
| **Display > Display Type**<br> | **Flow Panel**<br> |
| **Display > Type**<br> | **Section Panel**<br> |
| **Display > Orientation**<br> | **Vertical**<br> |

For example, the PWA screen in Smart IT such as theSHR:SV\_TicketDisplay formhas two flow panels with these properties.

## To set panels to scroll at different rates in Progressive Web Applications

1. In Developer Studio, open the form for which you want to create sticky panels.  
   For example, open theSHR:SV\_TicketDisplay form.
2. Select the Flow Panel Holder.  
   For example, in theSHR:SV\_TicketDisplay form, select panels with IDs 304428481 and 304436081.
3. In Properties, under**Display > Custom CSS Style,**add the following string:  
   **sticky-holder**  
   If there are previously existing values in the Custom CSS Style field, the string**sticky-holder**must be preceded by a space.
4. (*Optional*) If the form has horizontal navigation fields, remove the following string from the**Custom CSS Style**property:  
   **detach**
5. Click**Save**and sync the Mid Tier cache.  
   For more information about how to sync the cache, see[Synchronizing-Mid-Tier-cache](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Administering/Monitoring-the-system-and-performance/Configuring-cache-settings-for-the-Mid-Tier/Synchronizing-Mid-Tier-cache/).

## To validate the behavior of the panels in Progressive Web Applications

1. In a browser, log in to PWA.  
   **<*serverName*>:8080/arsys/pwa/#/login**
2. Change the URL to include the Progressive View form that you created in Developer Studio.  
   **<*serverName*>:8080/arsys/pwa/#/forms/<*serverName*>/<*formName*>/<*viewName*>**The panels in the PWA show 'sticky' behavior whenever there is more content in one of the panels.

## Troubleshooting

If the panels do not appear or if there is an issue with scrolling, perform the following steps:

* Confirm that the workflows and field properties are correctly defined in Developer Studio.
* If the page has horizontal navigation fields, remove the following string from the Custom CSS Style property:  
  **detach**