As a developer, you can create a table that can switch between selection modes. You can design a workflow that returns values which in turn are used by thePERFORM-ACTION-TABLE-ROW-SELECTION-MODEcommand to switch table lists between multiple selection, single selection, or view-only.

The following graphic shows the three selection modes that you can create for selection lists:

![image2021-5-26_12-43-2.png](.attachments/Creating-list-tables-and-setting-selection-mode-by-using-run-processes-in-Progressive-Web-Applicatio_image2021-5-26_12-43-2.png)

Related topics

[Using-Run-Process-and-PROCESS-commands](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-applications-by-using-Developer-Studio/Defining-workflow-to-automate-processes/Specifying-workflow-actions/Using-Run-Process-and-PROCESS-commands/)

[Creating-table-fields](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-applications-by-using-Developer-Studio/Developing-the-application-interface/Defining-tables-to-display-data/Creating-table-fields/)

## Before you begin

* You must have a basic understanding of progressive web applications and their development.  
  For more information, see[Developing-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/).
* You must create forms that contain the information that you want to display in the table.  
  In the following procedure, we map this form to the list table we create.
* You may have to define workflows that return values that can be used by thePERFORM-ACTION-TABLE-ROW-SELECTION-MODEcommand.

## To create a list table and set the selection mode by using a run process in a Progressive Web Application

### Step 1: To create a progressive view with a table showing information

1. InDeveloper Studio, create a regular form.
2. Create a Progressive View.

   <details class="confluence-expand-macro panel panel-default"><summary><span class="panel-title"><span class="title-text">Steps (2)</span></span></summary><div class="panel-body"><ol><li><strong>Form &gt; Create New View</strong>.<br/>The Create New View dialog box opens.</li><li>In the<strong>View Type</strong>list, select<strong>Progressive</strong>.<br/><img alt="image2021-2-18_11-11-57.png" data-xwiki-translated-attribute-thumbnail="true" height="103" src="../.attachments/Creating-list-tables-and-setting-selection-mode-by-using-run-processes-in-Progressive-Web-Applicatio_image2021-2-18_11-11-57.png"/></li></ol></div></details>
3. From the Palette, drag and drop**Table - List View**into the view.
4. In the Properties tab, at**Attributes > Tree/Table Property**, in the**Value**column, click the ellipsis (![image2021-2-18_11-33-49.png](.attachments/Creating-list-tables-and-setting-selection-mode-by-using-run-processes-in-Progressive-Web-Applicatio_image2021-2-18_11-33-49.png)) button.  
   The Tree/Table Property dialog opens.
5. Search for a form name and map the Table Columns to fields from a remote form.  
   For example if the table needs to show a list of departments and geographical locations, you can accordingly add remote forms with this information.
6. From the Palette, drag and drop**Button**into the view.  
   You can rename the button to indicate its function. In this example, rename it to**Multiple to Single Select**.
7. Save the form.

## Step 2: To create an active link and add the Run Process command

1. Select the button and create a new active link.  
   Select**New > Active Link**.
2. Select a server in the Select Server dialog box.  
   The Untitled Active Link screen appears.
3. In the Associated Forms section, click**Add**.  
   The Form Selector dialog box opens.
4. Select the form in the Progressive View which has the table and the button.
5. In**Active Link > Execution Options > Button/Menu****Field**, select the button that triggers the active link.
6. Right-click the**If Action**panel header.
7. Select**Add Action > Run Process**.
8. In the**Command Line**field, enter the following command:  
   PERFORM-ACTION-TABLE-ROW-SELECTION-MODE*selectionMode**tableFieldID*  
   Enter the following values of*selectionMode*to make a corresponding switch in selection modes of the lists:

   | Value of*selectionMode*<br> | Selection mode of list switches from<br> |
   | --- | --- |
   | 0<br> | Any selection mode to multiple selection mode<br> |
   | 1<br> | Any selection mode to to view-only<br> |
   | 2<br> | Any selection mode to to single selection<br> |

   In place of***tableFieldID***, you can also add**$*tableField*$**or**$*tableName*$**, where*tableField*and*tableName*are names of the table field table. The value of***selectionMode***can be passed by another field based on how you design active links but the values must be one among**0**,**2**, or**1**.
9. Save the active link.

## Results

When you display this form in progressive views, you can see a table list and a button that allows you to change the form, for example, multiple selection to a single selection, if you add**2**as the value of***selectionMode***in the command.

![image2021-5-20_16-9-43.png](.attachments/Creating-list-tables-and-setting-selection-mode-by-using-run-processes-in-Progressive-Web-Applicatio_image2021-5-20_16-9-43.png)