The @mention component is a typeahead feature introduced for Progressive views. This component is supported for the Character field, where you can type in to provide your inputs. You can set the metadata for this component by using Developer Studio.

When you define a menu for a Character field, the Enable Menu Hotkeys property is automatically set to**False**. However, any hotkey definitions created earlier remain as they are. You can't add any duplicate hotkey definitions. Ensure that the menu you attach to a hotkey is a Search Menu.

Related topics

[Process-commands](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-applications-by-using-Developer-Studio/Defining-workflow-to-automate-processes/Specifying-workflow-actions/Using-Run-Process-and-PROCESS-commands/Process-commands/)

[Field-Properties](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-applications-by-using-Developer-Studio/Developing-the-application-interface/Creating-and-managing-fields/Field-Properties/)

[Developing-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/)

[Using-Run-Process-and-PROCESS-commands](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-applications-by-using-Developer-Studio/Defining-workflow-to-automate-processes/Specifying-workflow-actions/Using-Run-Process-and-PROCESS-commands/)

Example

To understand how the @mention component works, consider a scenario where you're composing a new email in Microsoft Outlook for Office 365. As soon as you type**@**you get a list of users in your organization and the user that you select gets added to the**To**list. You also get additional information about the user, such as name, email address, and a display picture if available, which helps you identify the correct user when there are multiple users of the same name.

As a scenario specific toIS, if an incident manager is working with an incident, the incident manager can type**@**in the activity notes to get a list of agents. This helps the incident manager select a particular agent from the list of available agents.

To support the @mention component for Progressive views, the following properties are added in Developer Studio:

| Property name<br> | Property type<br> | Property values<br> | Description<br> |
| --- | --- | --- | --- |
| Enable Menu Hotkeys<br> | Boolean<br> | * True * False (Default) | Specifies if the menu hotkeys are to be enabled. To define menu hotkeys, you must set the value of this property to**True**.<br> |
| Menu Hotkeys<br> | String<br> | A string<br> | Use this property to define hotkey definitions. By default, the text "No Hotkey Defined" is displayed as the value for this property.<br> |

## To configure the @mention component

1. On the Progressive view of a form, double-click a Character field.
2. On the**Properties**panel, under the Display property group, for the Enable Menu Hotkeys property, select the**True**value.
3. In the**Value**column for the Menu Hotkeys property, click the ellipsis button.  
   The**Menu Hotkeys**dialog box is displayed.  
     
   ![menu-hotkeys.png](.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_menu-hotkeys.png)
4. Click**Add**, and then perform the following steps:

   | Column<br> | Step<br> |
   | --- | --- |
   | Hotkey<br> | Click the first row in this column, and then select a character from the list.<br> |
   | Menu Name<br> | Click the first row in this column, and then click the ellipsis button to select a menu from the**Menu Selector**dialog box.<br> |
   | Active Link<br> | Click the first row in this column, and then click the ellipsis button to select an active link from the**Active Link Selector**dialog box.<br>The active link that you attach to a hotkey must be an existing one and associated with the current form.<br> |
   | Labels<br> | Click the first row in this column, and then in the box, type in labels that are separated by a semicolon.<br> |
   | Auto Complete Key Stroke #<br> | Enter an integer value.<br> |
5. Click**OK**.

## Parameters for hotkey definition

The following parameters can be a part of any hotkey definition:

| Parameter<br> | Description<br> |
| --- | --- |
| Hotkey<br> | When you press this character key, the @mention component is executed based on the other parameters that you've provided in the hotkey definition. This parameter is the mandatory part of any @mention definition.<br> |
| Menu Name<br> | This is a name of the menu that is used to populate the popup. This parameter is the mandatory part of any @mention definition.<br> |
| Active Link<br> | This is a name of the active link that gets executed when you select an item from the popup. This parameter is an optional part of any @mention definition.<br> |
| Labels<br> | This is a set of labels that are defined for a menu. This parameter is an optional part of any @mention definition. You can add any text or you can add**$*menuLabel*$**where the label gets replaced by the menu label value during execution.*menuLabel*represents the label that is selected when using a search menu.<br> |
| Auto Complete Key Stroke #<br> | You can enter an integer value value for this parameter. For example, if you enter the value 3, a drop-down list appears after you type three characters in the menu. If you enter the value zero (0), the drop-down list appears as soon as type a hotkey character key.<br> |

There are scenarios when you want the users of your application to have the option of selecting the type of content that they see in an autosuggest list when using @mention. You can create such a search field by using theCHANGE\_HOTKEY\_MENUcommand.

## To enable users to select the type of content displayed in @mention

In the following example scenario, as an application developer, you add theCHANGE\_HOTKEY\_MENUcommand to enable the application users to decide the type of content in the @mention list.However, note that real-world implementations can vary considerably depending on your business needs.

Example:

**Problem**Apex Global wants to have a ticketing application in which one of the fields requires the application users to be able to use @mention to add mentions of either people or assets. The default behavior is that both assets and people are displayed in the @mention autosuggestion list. Apex Global wants the application users to be able to select an option to see only assets or only people for ease of use.

**Solution**Seth, the application developer, creates two buttons right next to the field. Users can click one button to make@mentionsuggest only assets or click the other button to make the @mention show only usernames. Seth uses a run processCHANGE\_HOTKEY\_MENU*fieldID key menuName*in an active link in each of the buttons so that the content displayed by the @mention autosuggest list is replaced by the content specified in the active link.

Before you begin

Make sure that you fulfil the following conditions before you perform the steps for creating fields where users can switch between @mention content.

* In Developer Studio, you must have a form that contains usernames and a form that contains asset names.
* You must have predefined search menus of type Search.

### Process for creating fields where users can switch between @mention content

The following diagram shows a high-level overview of the steps required to create fields where users can switch between different types of @mention content:

![image2022-7-27_9-21-53.png](.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_image2022-7-27_9-21-53.png)

Create two buttons and a character field. The character field consists of a default @mention menu. The buttons are assigned active links and menus which should replace the default @mention menu when the buttons are clicked by application users.  
The following animation explains a high-level concept of the use case:

To create the field and buttons

In this procedure, we create a character field with a default menu, two buttons that contain an active link that uses theCHANGE\_HOTKEY\_MENU.

1. In Developer Studio, create a New Regular Form.  
   ![image2022-7-20_20-10-36.png](.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_image2022-7-20_20-10-36.png)
2. Create a Progressive View.

   <details class="confluence-expand-macro panel panel-default"><summary><span class="panel-title"><span class="title-text">Steps (2)</span></span></summary><div class="panel-body"><ol><li><strong>Form &gt; Create New View</strong>.<br/><img alt="image2022-7-20_20-13-17.png" data-xwiki-image-style-border="true" data-xwiki-translated-attribute-thumbnail="true" src="../.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_image2022-7-20_20-13-17.png" width="250"/><br/>The Create New View dialog box opens.</li><li>In the<strong>View Type</strong>list, select<strong>Progressive</strong>.<br/><img alt="image2021-2-18_11-11-57.png" data-xwiki-translated-attribute-thumbnail="true" height="103" src="../.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_image2021-2-18_11-11-57.png"/></li></ol></div></details>
3. Add two buttons to the view.
4. Name the buttons as**Assets Only**and**Users Only**.
5. (*Optional*) Add a new section panel.

<details class="confluence-expand-macro panel panel-default"><summary><span class="panel-title"><span class="title-text">Steps (2)</span></span></summary><div class="panel-body"><ol><li><br/><ol><li>In<strong>Outline</strong>, right-click the section panel holder and select<strong>Add New Panel</strong>.<br/><strong><img alt="image2022-7-5_11-39-21.png" data-xwiki-translated-attribute-thumbnail="true" height="250" src="../.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_image2022-7-5_11-39-21.png"/></strong></li><li>In the Properties tab, select the Sub Panel Holder, and in Properties, click<strong>Display &gt; Orientation</strong>and select<strong>Horizontal</strong>.<br/>This changes the orientation to show the new section panel to the right of the section with the buttons.</li></ol></li></ol></div></details>

### To define the hotkey for the character field

1. Add a character field and add a hotkey associated with a search menu to it.
   1. From the Palette, drag**Character**into the view or the section panel.  
      Developer Studio assigns it a default name such as**Character Field\_c**.
   2. Select the character field and rename it to**Character Field**.  
      ![image2021-5-14_16-27-32.png](.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_image2021-5-14_16-27-32.png)
   3. In the Properties tab, click**Display > Enable Menu Hotkey**and select**True**.  
      This enabled you to set a hotkey for the character field.
   4. Below the**Enable Menu Hotkey**property, click the ellipsis (![image2021-2-18_11-33-49.png](.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_image2021-2-18_11-33-49.png)) button next to**Menu Hotkeys**.  
      The Menu Hotkeys dialog opens.
   5. Click**Add**.  
      Developer Studio adds**@**in the Hotkey column.

      **Best practice**  
      To fetch email IDs in the @mention options, you must add # as the hotkey instead of @ in the Hotkey column to avoid errors.
   6. In the Menu Name column, click the ellipsis (![image2021-2-18_11-33-49.png](.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_image2021-2-18_11-33-49.png)) button.  
      The Menu Selector dialog opens.
   7. Find the search menu that lists usernames and assets you want to associate with the hotkey and click**OK**.
   8. In the Auto Complete Key Stroke # column, add**3**.  
      The autosuggest is activated when application user types at least three characters.
   9. In the Properties tab, set a value in pixels for the**Hotkey Menu Max Height**property.  
      This is the maximum height of the @mention list when it displays a large number of results. The default value ofthe Hotkey Menu Max Height property is 200.

      **Best practice**  
      We recommend a value between 200 to 500 pixels for the**Hotkey Menu Max Height**property.
2. Save the form with a name.
3. In this example name the form as**ChangeHotkeyMenu**.

### To create a search menu that contains usernames

1. Create a new search menu.
2. Select**AR System Navigator >*aRServerName*> All Objects > Menus > New Search Menu**.  
   ![image2022-7-5_15-15-20.png](.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_image2022-7-5_15-15-20.png)  
   The hotkey supports only search menus.
3. Click the ellipsis (![image2021-2-18_11-33-49.png](.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_image2021-2-18_11-33-49.png)) button next to**Form Name**.  
   The Form Selector dialog opens.
4. Find and add the user form that contains all usernames, and click**OK**.
5. Save the search menu.  
   In this example, name the menu as**ChangeHotkeyMenuM1**.

### To create a search menu that contains asset names

1. Create another search menu and name it as**ChangeHotkeyMenuM2**.  
   This menu must list all asset names.
2. Click the ellipsis (![image2021-2-18_11-33-49.png](.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_image2021-2-18_11-33-49.png)) button next to**Form Name**.  
   The Form Selector dialog opens.
3. Find and add the form that contains all asset names, and click**OK**.
4. In the Label Fields section, click**Add**.  
   The Field Selector dialog opens.
5. Select Asset Name, and click**OK**.
6. Save the search menu.  
   In this example, name the menu as**ChangeHotkeyMenuM2**.

### To create an active link for the Users Only button

1. Create an active link for the**Users Only**button named**ChangehotkeymenuAL1**.
2. Select**New > Active Link**.  
   ![image2021-2-23_17-23-19.png](.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_image2021-2-23_17-23-19.png)
3. Add the following settings to the active link:

   | Setting<br> | Value, selection, or function<br> | Additional details<br> |
   | --- | --- | --- |
   | **Associated Forms > Add**<br> | **ChangeHotkeyMenu**<br> |  |
   | **Execution Options > Button/Menu Field**<br> | **Users**<br> | This is the button that triggers the active link.<br> |
   | **Run If Qualification**<br> | **1=1**<br> | This triggers the run process in the**If Actions**without exception.<br> |
   | **If Actions > Add action > Run Process**<br> | **CHANGE\_HOTKEY\_MENU*fieldID******@******changehotkeymenuM1*****$NULL$ $NULL$*****3***<br> | Make sure that there is a single space between each attribute.<br>*fieldID*is the ID of**Character Field**.<br>**changehotkeymenuM1**is not dynamic and must always be hardcoded (static). This active link runs when you type three characters, that is, when you type @ in the**Character Field**and it fetches information from the**ChangehotkeymenuM1**search menu.<br> |

To create an active link for the Assets Only button

1. Create another active link for the**Assets Only**button named**ChangehotkeymenuAL2**.
2. Select**New > Active Link**.
3. Add the following settings to the active link:

   | Setting<br> | Value, selection, or function<br> | Additional details<br> |
   | --- | --- | --- |
   | **Associated Forms > Add**<br> | **ChangeHotkeyMenu**<br> |  |
   | **Execution Options > Button/Menu Field**<br> | **Assets**<br> | This is the button that triggers the active link fetches and uses it to replace the default menu of the character field.<br> |
   | **Run If Qualification**<br> | **1=1**<br> | This triggers the run process in the**If Actions**without exception.<br> |
   | **If Actions > Add action > Run Process**<br> | **CHANGE\_HOTKEY\_MENU*fieldID******@******changehotkeymenuM2**activeLink1**labelsToShow**3***<br> | Make sure that there is a single space between each attribute.<br>*fieldID*is the ID of**Character Field**.<br>**changehotkeymenuM2**is not dynamic and must always be hardcoded (static) with the menu name. This active link runs when you type three characters, that is, when you type @ in the**Character Field**and it fetches information from the**ChangehotkeymenuM2**search menu.<br> |
4. Save the changes.

**Important**

In the case of rich text enabled fields, in the run process command, you can additionally specify the fields to be displayed in the @mention list as shown in the following example:

**CHANGE\_HOTKEY\_MENU*fieldID******@******changehotkeymenuM2**activeLink1**fieldID**3 $rtfLabel1$ $rtfLabel2$***

The***$rtfLabel1$***and***$rtfLabel2$***values are used to limit the display of @mention options list to just these two fields. If you do not specify any values, the first four fields available in the menu are displayed by default. You can specify up to four different values to be displayed in the @mention options list.

The following graphic illustrates the display of @mentions options with default information and when restricted to only employee name and email ID:

![with and without 002.png](.attachments/Adding-%40mention-for-fields-in-Progressive-Web-Applications_with-and-without-002.png)

Validating the character field in PWA

View the form in the progressive web application screen to check whether it works as intended.

1. In a browser, log in to PWA.  
   For example,**<*serverName*>:8080/arsys/pwa/#/login**
2. Change the URL to include the Progressive View form that you created in Developer Studio.  
   **<*serverName*>:8080/arsys/pwa/#/forms/<*serverName*>/<*formName*>/<progressiveV*iewName*>**
3. The PWA screen displays the character field and the buttons.
4. In**Character Field**, type**@**followed by three characters.  
   The field displays users and assets.
5. Click**Users Only**and type**@**followed by three characters.  
   The field displays usernames.
6. Click**Assets Only**and type**@**followed by three characters.  
   The field displays assets names.

## Where to go from here

Learn more about the syntax and additional options within the process command in the[Process-commands](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-applications-by-using-Developer-Studio/Defining-workflow-to-automate-processes/Specifying-workflow-actions/Using-Run-Process-and-PROCESS-commands/Process-commands/)topic.