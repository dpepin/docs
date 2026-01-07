provides a[localization toolkit](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/AR-System/ars221/Developing-applications/Localizing-an-application-to-other-languages/Using-the-localization-toolkit-to-localize-your-applications/)in Developer Studio to localize yourAR System serverapplications from English to other supported locales. Use the localization toolkit and the AR System Message Catalog form to localize your Progressive Web Application (PWA).  
  
The localization toolkit is used to extract the localizable strings from the objects. After extracting, export the strings to a Tab Separated Values (TSV) file, translate the strings and import the translated strings into the AR System Message Catalog form by using the ARMsgCatalogEntryCreator utility. This utility creates new records in the AR System Message Catalog form.The PWA screens use these records in the AR System Message Catalog form and display localized strings based on the browser locale.

Related topics

[Progressive View quick start guide](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Getting-started/Key-concepts/Application-development-overview/Progressive-View-quick-reference-guide/)

[Using the localization toolkit (Video)](https://www.youtube.com/watch?v=ztGN-amEf3A)

[Synchronizing-Mid-Tier-cache](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Administering/Monitoring-the-system-and-performance/Configuring-cache-settings-for-the-Mid-Tier/Synchronizing-Mid-Tier-cache/)

To localize a progressive web application, you don't need the static, locale-specific views created by the localization toolkit for standard applications. For PWA, the localization toolkit is used only to extract the localizable strings from the objects and to export the strings into a TSV file.

PWA uses the AR System Message Catalog form to store and retrieve translations as required. Thus, as a Remedy developer, you do not need to create locale-specific views for the same objects by using the new form.

If you are a ITSM user, you must configure a client gateway to access and customize your application by using Developer Studio.

Review the[Best practices for localizing a progressive web application](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Localizing-a-Progressive-Web-Application/#LocalizingaProgressiveWebApplication-localization)section below before you perform the localization process.

The following video (3:50) provides an overview of how to localize a Progressive Web Application.

[🎥 Watch Video: //www.youtube.com/watch?v=t-3YfIcljjU](//www.youtube.com/watch?v=t-3YfIcljjU)

![icon_play.png](.attachments/Localizing-a-Progressive-Web-Application_icon_play.png)<https://youtu.be/t-3YfIcljjU>

PWA supports the following languages out-of-the-box:

* en—English (default)
* de—German
* es—Spanish
* fr—French
* iw\_IL—Hebrew
* it—Italian
* ja- Japanese
* ko-Korean
* pt\_BR—Portuguese
* ru—Russian
* zh\_CN—Chinese

If you want to localize your Progressive Web Application in any other language, use the following localization process.

## Localization process

Perform the following steps in Developer Studio to complete the localization process:

![localization-process.png](.attachments/Localizing-a-Progressive-Web-Application_localization-process.png)

1. Prepare your application that you want to localize.
2. Install the localization toolkit.
3. Set a root folder.
4. Create a package definition for the forms that you want to localize.
5. Extract the strings that you want to localize.
6. Export the strings in a file that has the default Tab Separated Values (TSV) format.
7. Translate the strings in the TSV file.
8. Import the TSV file to the AR System Message Catalog form.

## To prepare your application that you want to localize

To be ready for localization, your server must be configured for localization. Additionally, applications must have the correct localization properties set for forms, their associated views, and fields. By default, all forms, views, and fields are configured to be localized, so you should not have to manually set each property. Conversely, if you have specific forms, views, or fields that you*do not*want localized, set the property accordingly.

For instructions, see[Preparing-your-application-to-be-localized](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/AR-System/ars221/Developing-applications/Localizing-an-application-to-other-languages/Using-the-localization-toolkit-to-localize-your-applications/Preparing-your-application-to-be-localized/).

## To install the localization toolkit

When you install the localization toolkit, the localization toolkit files are added to the**DeveloperStudio**folder of your AR System installation. (The default installation directory is**C:\Program Files\ Software\ARSystem\ DeveloperStudio**.)

The localization toolkit plug-ins are placed in the**plugins**folder with the other Developer Studio plug-ins. A Localization Package Definitions branch is added to each server in the AR System Navigator in Developer Studio.

For instructions, see[Installing-the-localization-toolkit](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/AR-System/ars221/Developing-applications/Localizing-an-application-to-other-languages/Using-the-localization-toolkit-to-localize-your-applications/Installing-the-localization-toolkit/).

## To set a root folder

To begin the localization process, set a root folder, which stores:

* The localization database (**l10n.db**)
* The log file that logs the translation progress (**l10n.log**)
* Package definition files that you create for translation

The default root folder is the*BMCRemedyDeveloperStudioInstallDir***\workspace\l10N**folder.

For instructions, see[Setting-a-root-folder](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/AR-System/ars221/Developing-applications/Localizing-an-application-to-other-languages/Using-the-localization-toolkit-to-localize-your-applications/Setting-a-root-folder/).

## To create a package definitions for the forms

The Localization Package Definition editor in Developer Studio makes it easy to create a localization package definition for your application and any other forms that you want in the package definition.

For instructions, see[Creating-a-localization-package-definition](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/AR-System/ars221/Developing-applications/Localizing-an-application-to-other-languages/Using-the-localization-toolkit-to-localize-your-applications/Creating-a-localization-package-definition/).

## To extract the strings that you want to localize

After you create a localization package definition, you can extract the strings for localization into the localization database (**l10n.db**in the root folder).

For instructions, see[Extracting-the-strings-for-localization](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/AR-System/ars221/Developing-applications/Localizing-an-application-to-other-languages/Using-the-localization-toolkit-to-localize-your-applications/Extracting-the-strings-for-localization/).

## To export the extracted strings to a TSV file

For Progressive Views, you must use the TSV format.

**Important**

* While exporting strings for localization, you can opt to export only the items that are related with Progressive Views.
* The time taken to extract or export strings depends upon the number of items involved. Therefore, it can take a while to export large number of items, for example, 1000 or 2000.
* You cannot use a TSV file to import translations through the localization toolkit. This file is generated specifically for the AR System Message Catalog form. Use the[command-line utility](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Localizing-a-Progressive-Web-Application/#LocalizingaProgressiveWebApplication-ImportTSVFile)to import a TSV file in to the AR System Message Catalog form after translation.

Perform the following steps:

1. In Developer Studio, open the localization package definition.
2. Click**Export Strings**.
3. In the Localization Item Export dialog box, enter the full path to a target**.tsv**file that will contain the extracted strings.  
   If the path you enter does not have a TSV file, then it is created. If you specify a full path, the file is created at that location. If you specify only a file name, the file is created in the root folder.  
   The default root folder is the*BMCRemedyDeveloperStudioInstallDir***\workspace\l10N**folder.
4. Select the locale you want to export.
5. Select the state of the strings that you want to export.
6. Click**OK**.  
   Only those items that are set to the state you selected in step 5 (for example, "Ready to Translate") are exported to the**.tsv**file. For more information, see[Reviewing the status of the translation progress](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/AR-System/ars221/Developing-applications/Localizing-an-application-to-other-languages/Using-the-localization-toolkit-to-localize-your-applications/Reviewing-the-translations/).

   **Tip**

   For each locale, add a new column with localized strings that map to the**Source Text**column to the exported file. Add the locale code to the header of the new localized column.

## Tab Separated Values (TSV) file

The following image shows a sample**TSV**file*before translation*:

![before-translation.png](.attachments/Localizing-a-Progressive-Web-Application_before-translation.png)

The following table provides information about the columns in the exported TSV file:

| Column name<br> | Description<br> |
| --- | --- |
| Message-Type<br> | The type of the object for which the string is extracted.<br>See[Types of objects exported](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Localizing-a-Progressive-Web-Application/#LocalizingaProgressiveWebApplication-TOEO).<br> |
| Form Name/Message ID<br> | The name of the Form or Active Link or Filter<br> |
| VUI ID<br> | The View ID of the Form<br> |
| Field ID/Message Num<br> | Field ID or message number from the Active Link or Filter actions<br> |
| Source Text<br> | The string to be localized. It includes the following:<br>  * Field labels, such as Data Fields, Control Fields, and Selection Fields * Selection alias for fields such as Radio button and Drop-down list * Help text from forms and fields * Alternative text for fields * Message strings from Active Links and Filters |

**Important**

In a TSV file, characters such as comma (,) are replaced by tags such as <comma> in strings.

Because TSV is a delimiter-separated file, characters such as commas or new lines in the file result in localization strings occupying multiple cells and rows instead of just one cell. Therefore, these are replaced by tags as shown in the following table:

| Character<br> | Description<br> | Tag used<br> |
| --- | --- | --- |
| \r\n<br> | Carriage return and new line<br> | <crlf><br> |
| \n<br> | New line<br> | <lf><br> |
| \r<br> | Carriage return<br> | <cr><br> |
| ,<br> | Comma<br> | <comma><br> |

### Types of objects exported

<details class="confluence-expand-macro panel panel-default"><summary><span class="panel-title"><span class="title-text">Click here to see the types of objects currently exported in a TSV file</span></span></summary><div class="panel-body"><table><thead><tr><th scope="col"><div><p>Message type</p></div></th><th scope="col"><div><p>Type of object</p></div></th><th scope="col"><div><p>Description of the string</p></div></th></tr></thead><tr><td><div><p>0</p></div></td><td><div><p>System Message</p></div></td><td><div><p>Belongs to a System message action.</p></div></td></tr><tr><td><div><p>1</p></div></td><td><div><p>Active Link Message</p></div></td><td><div><p>Belongs to an Active Link message action.</p></div></td></tr><tr><td><div><p>2</p></div></td><td><div><p>Filter Message</p></div></td><td><div><p>Belongs to a Filter message action.</p></div></td></tr><tr><td><div><p>3</p></div></td><td><div><p>Active Link Help Text</p></div></td><td><div><p>Belongs to the Help Text property of an Active Link.</p></div></td></tr><tr><td><div><p>4</p></div></td><td><div><p>Form Help Text</p></div></td><td><div><p>Belongs to the Help Text property of a Form.</p></div></td></tr><tr><td><div><p>5</p></div></td><td><div><p>Field Help Text</p></div></td><td><div><p>Belongs to the Help Text property of a Field.</p></div></td></tr><tr><td><div><p>6</p></div></td><td><div><p>Container Description</p></div></td><td><div><p>Belongs to the Description property of a Container.</p></div></td></tr><tr><td><div><p>7</p></div></td><td><div><p>List Menu Definition</p></div></td><td><div><p>Belongs to the Definition property of a List Menu.</p></div></td></tr><tr><td><div><p>8</p></div></td><td><div><p>External Report</p></div></td><td><div><p>Belongs to an External Report.</p></div></td></tr><tr><td><div><p>9</p></div></td><td><div><p>Container Label</p></div></td><td><div><p>Belongs to the Label property of a Container.</p></div></td></tr><tr><td><div><p>10</p></div></td><td><div><p>Container Help</p></div></td><td><div><p>Belongs to the Help property of a Container.</p></div></td></tr><tr><td><div><p>11</p></div></td><td><div><p>Application Help</p></div></td><td><div><p>Belongs to the Help property of an Application.</p></div></td></tr><tr><td><div><p>12</p></div></td><td><div><p>Application About</p></div></td><td><div><p>Belongs to the About property of an Application.</p></div></td></tr><tr><td><div><p>13</p></div></td><td><div><p>Application Help Index</p></div></td><td><div><p>Belongs to the Help Index property of an Application.</p></div></td></tr><tr><td><div><p>14</p></div></td><td><div><p>Flashboards System Message</p></div></td><td><div><p>Belongs to the System Message property of Flashboards.</p></div></td></tr><tr><td><div><p>15</p></div></td><td><div><p>Flashboards Label</p></div></td><td><div><p>Belongs to the Label property of Flashboards.</p></div></td></tr><tr><td><div><p>16</p></div></td><td><div><p>Field Label</p></div></td><td><div><p>Belongs to the Label property of a Field.</p></div></td></tr><tr><td><div><p>17</p></div></td><td><div><p>Field Help Text</p></div></td><td><div><p>Belongs to the Help Text property of a Field.</p></div></td></tr><tr><td><div><p>18</p></div></td><td><div><p>Alternative Text</p></div></td><td><div><p>Belongs to the Alternative Text property of a Field.</p></div></td></tr><tr><td><div><p>19</p></div></td><td><div><p>Selection Alias</p></div></td><td><div><p>Belongs to the Alias property of a Selection Field.</p></div></td></tr><tr><td><div><p>20</p></div></td><td><div><p>Label for Empty Value</p></div></td><td><div><p>Belongs to the Empty Value property of a Label.</p></div></td></tr><tr><td><div><p>21</p></div></td><td><div><p>Alias Singular</p></div></td><td><div><p>Belongs to the Singular property of an Alias Field.</p></div></td></tr><tr><td><div><p>22</p></div></td><td><div><p>Alias Plural</p></div></td><td><div><p>Belongs to the Plural property of an Alias Field.</p></div></td></tr><tr><td><div><p>23</p></div></td><td><div><p>Alias Short Singular</p></div></td><td><div><p>Belongs to the Short Singular property of an Alias Field.</p></div></td></tr><tr><td><div><p>24</p></div></td><td><div><p>Alias Short Plural</p></div></td><td><div><p>Belongs to the Short Plural property of an Alias Field.</p></div></td></tr><tr><td><div><p>25</p></div></td><td><div><p>Entrypoint Label Default New</p></div></td><td><div><p>Belongs to the Default New property of an Entrypoint Label.</p></div></td></tr><tr><td><div><p>26</p></div></td><td><div><p>Entrypoint Label Default Search</p></div></td><td><div><p>Belongs to the Default Search property of an Entrypoint Label.</p></div></td></tr><tr><td><div><p>27</p></div></td><td><div><p>Attach Add Label</p></div></td><td><div><p>Belongs to the Add Label property of an Attach Field.</p></div></td></tr><tr><td><div><p>28</p></div></td><td><div><p>Attach Delete Label</p></div></td><td><div><p>Belongs to the Delete Label property of an Attach Field.</p></div></td></tr><tr><td><div><p>29</p></div></td><td><div><p>Attach Display Label</p></div></td><td><div><p>Belongs to the Display Label property of an Attach Field.</p></div></td></tr><tr><td><div><p>30</p></div></td><td><div><p>Attach Save Label</p></div></td><td><div><p>Belongs to the Save Label property of an Attach Field.</p></div></td></tr><tr><td><div><p>31</p></div></td><td><div><p>Attach File Name Title</p></div></td><td><div><p>Belongs to the File Name Title property of an Attach Field.</p></div></td></tr><tr><td><div><p>32</p></div></td><td><div><p>Attach File Size Title</p></div></td><td><div><p>Belongs to the File Size Title property of an Attach Field.</p></div></td></tr><tr><td><div><p>33</p></div></td><td><div><p>Attach Label Title</p></div></td><td><div><p>Belongs to the Label Title property of an Attach Field.</p></div></td></tr><tr><td><div><p>34</p></div></td><td><div><p>Attach Deselect Label</p></div></td><td><div><p>Belongs to the Deselect Label property of an Attach Field.</p></div></td></tr><tr><td><div><p>35</p></div></td><td><div><p>Button Text</p></div></td><td><div><p>Belongs to the Text property of a Button.</p></div></td></tr><tr><td><div><p>36</p></div></td><td><div><p>Menu Text</p></div></td><td><div><p>Belongs to the Text property of a Menu.</p></div></td></tr><tr><td><div><p>37</p></div></td><td><div><p>Menu Help</p></div></td><td><div><p>Belongs to the Help property of a Menu.</p></div></td></tr><tr><td><div><p>38</p></div></td><td><div><p>Tooltip</p></div></td><td><div><p>Belongs to the Text property of a Button.</p></div></td></tr><tr><td><div><p>39</p></div></td><td><div><p>HTML Text</p></div></td><td><div><p>Belongs to the Text property of HTML.</p></div></td></tr><tr><td><div><p>40</p></div></td><td><div><p>Enums Labels</p></div></td><td><div><p>Belongs to the Labels property of an Enumeration.</p></div></td></tr><tr><td><div><p>41</p></div></td><td><div><p>Text</p></div></td><td><div><p>Belongs to the Text property.</p></div></td></tr><tr><td><div><p>42</p></div></td><td><div><p>Table Selection Column Label</p></div></td><td><div><p>Belongs to the Column Label property of a Table Selection.</p></div></td></tr><tr><td><div><p>43</p></div></td><td><div><p>Table Root Node Alternative Text</p></div></td><td><div><p>Belongs to the Alternative Text property of a Table Root Node.</p></div></td></tr><tr><td><div><p>44</p></div></td><td><div><p>Table Entries Returned</p></div></td><td><div><p>Belongs to the Entries Returned property of a Table.</p></div></td></tr><tr><td><div><p>45</p></div></td><td><div><p>Table Refresh</p></div></td><td><div><p>Belongs to the Refresh property of a Table.</p></div></td></tr><tr><td><div><p>46</p></div></td><td><div><p>Table Delete</p></div></td><td><div><p>Belongs to the Delete property of a Table.</p></div></td></tr><tr><td><div><p>47</p></div></td><td><div><p>Table Report</p></div></td><td><div><p>Belongs to the Report property of a Table.</p></div></td></tr><tr><td><div><p>48</p></div></td><td><div><p>Table Select All</p></div></td><td><div><p>Belongs to the Select All property of a Table.</p></div></td></tr><tr><td><div><p>49</p></div></td><td><div><p>Table Deselect All</p></div></td><td><div><p>Belongs to the Deselect All property of a Table.</p></div></td></tr><tr><td><div><p>50</p></div></td><td><div><p>Table Preference</p></div></td><td><div><p>Belongs to the Preference property of a Table.</p></div></td></tr><tr><td><div><p>51</p></div></td><td><div><p>Table Chunk Next</p></div></td><td><div><p>Belongs to the Chunk Next property of a Table.</p></div></td></tr><tr><td><div><p>52</p></div></td><td><div><p>Table Chunk Previous</p></div></td><td><div><p>Belongs to the Chunk Previous property of a Table.</p></div></td></tr><tr><td><div><p>53</p></div></td><td><div><p>Row Label</p></div></td><td><div><p>Belongs to the Label property of a Row.</p></div></td></tr><tr><td><div><p>54</p></div></td><td><div><p>Row Label Plural</p></div></td><td><div><p>Belongs to the Label Plural property of a Row.</p></div></td></tr><tr><td><div><p>55</p></div></td><td><div><p>Table Auto Refresh</p></div></td><td><div><p>Belongs to the Auto Refresh property of a Table.</p></div></td></tr><tr><td><div><p>56</p></div></td><td><div><p>Table Unread</p></div></td><td><div><p>Belongs to the Unread property of a Table.</p></div></td></tr><tr><td><div><p>57</p></div></td><td><div><p>Table Read</p></div></td><td><div><p>Belongs to the Read property of a Table.</p></div></td></tr><tr><td><div><p>58</p></div></td><td><div><p>Table Not Refresh</p></div></td><td><div><p>Belongs to the Not Refresh property of a Table.</p></div></td></tr><tr><td><div><p>59</p></div></td><td><div><p>Tree Table Custom Value</p></div></td><td><div><p>Belongs to the Custom Value property of a Tree Table.</p></div></td></tr><tr><td><div><p>101</p></div></td><td><div><p>Message</p></div></td><td><div><p>Belongs to the Message property.</p></div></td></tr><tr><td><div><p>102</p></div></td><td><div><p>Data</p></div></td><td><div><p>Belongs to the Data property.</p></div></td></tr><tr><td><div><p>103</p></div></td><td><div><p>Entry Point</p></div></td><td><div><p>Belongs to the Entry Point property.</p></div></td></tr><tr><td><div><p>104</p></div></td><td><div><p>Menu</p></div></td><td><div><p>Belongs to the Menu property.</p></div></td></tr><tr><td><div><p>105</p></div></td><td><div><p>Description</p></div></td><td><div><p>Belongs to the Description property.</p></div></td></tr><tr><td><div><p>106</p></div></td><td><div><p>Guide Help Text</p></div></td><td><div><p>Belongs to the Help Text property of a Guide.</p></div></td></tr><tr><td><div><p>107</p></div></td><td><div><p>App Help Text</p></div></td><td><div><p>Belongs to the Help Text property of an Application.</p></div></td></tr></table></div></details>

## To translate the strings in a TSV file

Send the exported TSV file to a vendor for translation.

**Best practice**  
For accurate translation, we recommend that you send the file to professional translators. (Open source and commercial editors are available for purchase by several third-party vendors.)

After the translation is completed, the TSV file has an additional sixth column which contains all the translations. The TSV file contains localized strings starting from the sixth column. That is, each column represents a single locale.

The following image shows a sample**TSV**file*after translation*:

![after-translation.png](.attachments/Localizing-a-Progressive-Web-Application_after-translation.png)

## To import a TSV file containing translated strings to the AR System Message Catalog Form

You can use the ARMsgCatalogEntryCreator utility that reads the TSV file and creates or updates an entry in the AR System Message Catalog form. The ARMsgCatalogEntryCreator utility accepts only a TSV file as an input.

Perform the following steps to import a TSV file to the AR System Message Catalog form using the ARMsgCatalogEntryCreator utility:

1. Before you use this utility, sort the TSV file four times—first by the Form Name column, next by the Field ID column, next by the View ID column, and finally by the Message Type column.

   **Important**

   Make sure that yourAR System serversupports the locale that you want to translate to. Otherwise, records with corrupted data, instead of the actual data, might get created in the AR System Message Catalog form.
2. Navigate to**<ARSystemInstallDir>/ARSystem/artools**and find the**armsgcatalogentrycreator.bat**file.
3. From a command prompt, run the**armsgcatalogentrycreator.bat**file by using the following command:

   ARMsgCatalogEntryCreator utility command syntaxarmsgcatalogentrycreator.bat [x] [u] [p] [t] [f]ARMsgCatalogEntryCreator utility command examplearmsgcatalogentrycreator.batf<LocationofTSV file>\Translations.tsvu<Username>x<Server Name>

   The following table describes the inputs for the Command Line Interface (CLI) and parameters for connecting to the AR System:

   <details class="confluence-expand-macro panel panel-default"><summary><span class="panel-title"><span class="title-text">Parameter descriptions</span></span></summary><div class="panel-body"><table><thead><tr class=""><th scope="col"><div><p>Parameter</p></div></th><th scope="col"><div><p>Description</p></div></th></tr></thead><tr class=""><td><div><p>x</p></div></td><td><div><p>Name of the server to connect to.</p></div></td></tr><tr class=""><td><div><p>u</p></div></td><td><div><div class="content-wrapper"><p>Name that identifies the user account for the<span>AR System server</span>.</p></div></div></td></tr><tr class=""><td><div><p>p</p></div></td><td><div><p>Password for the user account.</p><p>If you have a blank password, you can ignore this option.</p></div></td></tr><tr class=""><td><div><p>t</p></div></td><td><div><p>TCP port number to connect to.</p><p>If the port number is unknown, use<span class="box"><span class="code">t 0</span></span>.</p></div></td></tr><tr class=""><td><div><p>f</p></div></td><td><div><p>Name of the TSV file.</p></div></td></tr></table><p>Depending upon the row data, an entry is created or updated. For every locale, a separate entry is created per row. For example, a single row entry in the TSV file with three translations (that is, three different locales) creates three new entries for that string.</p></div></details>
4. On the**Cache Settings**page of the Mid Tier Configuration Tool, click**Flush Cache**.

**Important**

The Selection Alias type of object (Message type 19) is handled in a special way. Suppose, there is a Selection Alias type of object called "Status" that has five aliases as New, Assigned, Fixed, Rejected, and Close. For each alias, instead of creating a separate entry, the aliases are combined into a single record.

For example:

{"New":"Neu","Assigned":"Zugewiesen","Fixed":"Fest","Rejected":"Abgelehnt","Closed":"Geschlossen"}

In this example, each alias is separated by a comma (,) and contains two values—the left one is the actual string that is being exported and the right one is the translated string.

**Important**

In the TSV file, columns after the Source Text column hold the translated data. If the translated data column for a language has the*same string*as the Source Text (English) column, the ARMsgCatalogEntryCreator utility does not create a record for the same string in the AR System Message Catalog Form.

For example, if you have a string 'ALL' in the English and the Russian language columns, the utility skips creating a new record for the string 'ALL' for the Russian language column.

This is applicable for all message types except**19 (Selection Field)**as all the values are combined in a single record.

## Best practices for localizing a progressive web application

* Use independent forms only so that the related Active Links and Filters are also considered.
* For the form fields that you want to localize, set the value of the "Localize Label" property in Display Properties to**True**.
* When you delete a package definition, the package definition is deleted, but the extracted strings are not deleted from the localization database. If you create a package definition with the same name as the deleted one and export, you get the extracted strings from the deleted package definition as well. To avoid this issue, we recommend that you explicitly delete those strings from the database.