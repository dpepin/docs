The Progress bar widget is a component that you can configure to show the progress of a particular event or the steps of a particular process. You can also configure it to show the milestones on a timeline. For example, you can use this widget to display the status of your ticket. Mid Tier displays this widget on a form for which a progressive view is enabled. In Developer Studio, you can enable the Progress bar widget by adding a table, and then setting the Display Type of the table to**Progress Bar View**.

A table on a form represents one Progress bar on the UI and the number of rows in that table represent the number of nodes on the Progress bar.

Related topics

[Developing-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/)

[Defining-tables-to-display-data](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-applications-by-using-Developer-Studio/Developing-the-application-interface/Defining-tables-to-display-data/)

[Flow-panel-holders-for-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Flow-panel-holders-for-Progressive-Web-Applications/)

The following video (3:37) describes how to configure and use the progress bar widget:

[🎥 Watch Video: https://www.youtube.com/watch?v=-T90EgZ\_ZtI](https://www.youtube.com/watch?v=-T90EgZ_ZtI)

![icon_play.png](.attachments/Configuring-the-Progress-bar-widget-in-Progressive-Web-Applications_icon_play.png)<https://youtu.be/-T90EgZ_ZtI>

The following image shows the Progress bar widget:

![progress-bar-widget.png](.attachments/Configuring-the-Progress-bar-widget-in-Progressive-Web-Applications_progress-bar-widget.png)

## Before you begin

* To configure a Progress bar widget, you must have a minimum of six columns selected from a table.
* You must define the mappings for all columns.
* You can't define a duplicate mapping.

## To configure the Progress bar widget

1. On the progressive view of a form, double-click a Table field.
2. On the**Properties**panel, under the Display property group, for the Display Type property, select the**Progress Bar View**value.
3. In the**Value**column for the Tree/Table Property property, click the ellipsis button.  
   The**Tree/Table Property**dialog box is displayed.  
     
   ![tree-table-property-dialog-box.png](.attachments/Configuring-the-Progress-bar-widget-in-Progressive-Web-Applications_tree-table-property-dialog-box.png)
4. Perform the following steps:
   1. In the**Form Name**box, add any form from where you want to fetch the data in the table.
   2. In the**Qualification**box, add a condition as per your requirement.
   3. Add the minimum required six columns for the mappings.  
      You can add any additional columns, if required.
   4. Click**OK**.
5. Click a column in the table.
6. On the**Properties**panel, under the Display property group, in the Progressbar Field property, define the required mappings such as title, status, and instance ID.
7. Double-click the Table field.
8. *(Optional)*On the**Properties**panel, under the Display property group, for the Mapping Identifier property, enter a value.  
   If you don't specify any value, the default colors are displayed on a Progress bar. To learn how to define a color for the Progress bar, see[AR System Progress Bar Widget Mapping form](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Configuring-the-Progress-bar-widget-in-Progressive-Web-Applications/#ConfiguringtheProgressbarwidgetinProgressiveWebApplications-PBWidget).
9. *(Optional)*On the**Properties**panel, under the Display property group, for the**Show Date As**property, select any option.  
   You can specify whether the tooltips on the SLA progress bardisplayabsolute dates, relative dates, or both.

## AR System Progress Bar Widget Mapping form

While designing a Progress bar, if you want to define a color for the Progress bar based on certain rules, you can use the AR System Progress Bar Widget Mapping form. The value in the**Mapping Identifier**box on this form must match the value for the Mapping Identifier property in Developer Studio. You can use this form before or after setting the properties for the Progress bar in Developer Studio.

The following table provides information about the fields available on the AR System Progress Bar Widget Mapping form:

| Field name<br> | Field type<br> | Description<br> |
| --- | --- | --- |
| Mapping Identifier<br> | Character<br> | Specifies the value that you must provide for the in a table to attach a mapping.<br> |
| Status Value<br> | Character<br> | Specifies the status value for which you want to set the bar color.<br> |
| Progress Bar Color<br> | Selection:<br>  * Danger * Success * Warning * Info * Inactive | Specifies the color of the bar for the provided status value.<br> |
| Precedence<br> | Integer<br> | Specifies the precedence for the overall status of the bar, in case there are multiple SLTs on the same bar.<br> |
| Node Icon<br> | Selection:<br>  * Check * Cross * None | Specifies the icon for the node on the progress bar.<br> |
| Node Fill Color<br> | Selection:<br>  * Danger * Success * Warning * Info * Inactive * None | Specifies the color for the node on the progress bar.<br> |