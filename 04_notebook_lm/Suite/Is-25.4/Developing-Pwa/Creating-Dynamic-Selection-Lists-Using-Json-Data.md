Fetch JSON data and pass it to a character menu inDeveloper Studioto create a list or to populate a field in Progressive Web Applications. Use this method of creating dynamic selection lists in situations where the content to be displayed varies according to various user actions and settings. You can fetch JSON data by using webhooks, REST filters, or active links.

The following example procedure demonstrates:

* How to use the**JSON Menu Label**,**JSON Menu Value**, and**JSON Field ID**properties in a character field to extract values from JSON data and display the data as a list.
* How to create an active link that uses the JSONMAP function to extract a specific value from JSON data and display it in a character field.

This example shows how the**JSON Menu Label**,**JSON Menu Value**, and**JSON Field ID**properties, and the JSONMAP function work. However, note that real-world implementations can vary considerably depending on your business needs.

The following video (4:06) explains the concept and also demonstrates how the JSON properties and the JSONMAP function works:

[🎥 Watch Video: https://www.youtube.com/watch?v=3eRIML5mOgI](https://www.youtube.com/watch?v=3eRIML5mOgI)

![icon-play.png](.attachments/Creating-dynamic-selection-lists-for-Progressive-Web-Applications-by-using-JSON-data_icon-play.png)<https://youtu.be/3eRIML5mOgI>

## Before you begin

* You must have a basic understanding of progressive web applications and their development. For more information, see[Developing-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/).
* You must know how to fetch JSON data by using workflows that have webhooks, REST filters, or active links.
* You can download the[JSONMAP\_example\_fields.def](https://docs.bmc.com/xwiki/bin/download/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Creating-dynamic-selection-lists-for-Progressive-Web-Applications-by-using-JSON-data/WebHome/JSONMAP_example_fields.def?rev=1.1)file and import it intoDeveloper Studioto create the fields and settings described in the following procedure.

## To create a dynamic selection list for progressive web applications by using JSON data

1. InDeveloper Studio, create a New Regular Form.
2. Create a Progressive View.

   <details class="confluence-expand-macro panel panel-default"><summary><span class="panel-title"><span class="title-text">Steps (2)</span></span></summary><div class="panel-body"><ol><li>Select<strong>Form &gt; Create New View</strong>.<br/>The Create New View dialog box opens.</li><li>In the<strong>View Type</strong>list, select<strong>Progressive</strong>.<br/><img alt="image2021-2-18_11-11-57.png" data-xwiki-translated-attribute-thumbnail="true" height="103" src="../.attachments/Creating-dynamic-selection-lists-for-Progressive-Web-Applications-by-using-JSON-data_image2021-2-18_11-11-57.png"/></li></ol></div></details>
3. Drag four character fields into the view.  
   In this example, name the fields**JSON**,**Json Exp**,**Output**, and**Character Field**.  
   ![image2021-6-2_14-30-43.png](.attachments/Creating-dynamic-selection-lists-for-Progressive-Web-Applications-by-using-JSON-data_image2021-6-2_14-30-43.png)
4. In the Properties pane, change the**Display Type**property of the character fields to**Drop-Down List**.
5. Select the**JSON**field, and in the**Properties**tab, change the**Database > Input Length**to**0**.  
   Setting**Input Length**at a value of**0**enables the field to store content of any length.  
   In real-world scenarios, the**JSON**field receives the JSON data automatically by means of a workflow or a webhook that you have already defined. Also, the field may be hidden from the Progressive View because it simply holds the JSON data. In this example, we manually paste JSON data into the**JSON**field in Progressive View.
6. Select**Character Field**from the view and in the**Properties**tab, add the following values under**Attributes**:

   | Property<br> | Value<br> |
   | --- | --- |
   | **JSON Menu Label**<br> | **#colors[\*].color#+#colors[\*].category**<br> |
   | **JSON Menu Value**<br> | **colors[\*].id**<br> |
   | **JSON Field ID**<br> | The field ID of the**JSON**field<br> |

   The**Character Field**displays menu labels of the format color and category.
7. In the**Menu Style**list, select**Append**.  
   This option displays the**Character Field**in Progressive View as a list where you can select multiple options.
8. Define a button that runs the active links that you defined for the**Output**field.  
   ![image2021-6-2_14-32-46.png](.attachments/Creating-dynamic-selection-lists-for-Progressive-Web-Applications-by-using-JSON-data_image2021-6-2_14-32-46.png)
9. Select the**Extract Value**button field in the view and add an active link with the following settings:

   | Setting<br> | Value, selection, or function<br> |
   | --- | --- |
   | **If Actions**<br> | **Set Fields**<br> |
   | **Data Source**<br> | **CURRENT SCREEN**<br> |
   | **Field**<br> | **Output**<br> |
   | **Value**<br> | JSONMAP($JSON$, $Json Exp$) |

   This field uses the JSONMAP function, which picks up the data from the**JSON**field and the expression that you enter in the**Json Exp**field, and displays it in the**Output**field.
10. Select the**Character Field**from the view and define an active link with the following settings:

    | Setting<br> | Value, selection, or function<br> |
    | --- | --- |
    | **Execution Options > Field**<br> | **Character Field**<br> |
    | **Menu Choice**<br> | **Selected**<br> |
    | **If Actions**<br> | **Set Fields**<br> |
    | **Data Source**<br> | **CURRENT SCREEN**<br> |
    | **Field**<br> | **Output**<br> |
    | **Value**<br> | **JSONMAP($JSON$, $Json Exp$)**<br> |

    This active link runs when you select any item in the**Character Field**list in Progressive View, and displays the output of the JSONMAP function in the**Output**field.
11. Save the changes.

## Validating the selection list in Progressive View

1. In a browser, log in to PWA.  
   **<*serverName*>:8080/arsys/pwa/#/login**
2. Change the URL to include the Progressive View form that you created inDeveloper Studio.**<*serverName*>:8080/arsys/pwa/#/forms/<*serverName*>/<*formName*>/<*viewName*>**
3. Paste the following example JSON to the**JSON**field.

   <details class="confluence-expand-macro panel panel-default"><summary><span class="panel-title"><span class="title-text">Example JSON</span></span></summary><div class="panel-body"><div class="box"><div class="code"><span>"colors"</span>: [<br/><span>{</span><br/><span>"id"</span>:<span>1</span>,<br/><span>"color"</span>:<span>"black"</span>,<br/><span>"category"</span>:<span>"hue"</span>,<br/><span>"type"</span>:<span>"primary"</span>,<br/><span>"code"</span>:<span>{</span><br/><span>"rgba"</span>: [<span>255</span>,<span>255</span>,<span>255</span>,<span>1</span>],<br/><span>"hex"</span>:<span>"#000"</span><br/><span>}</span><br/><span>}</span>,<br/><span>{</span><br/><span>"id"</span>:<span>2</span>,<br/><span>"color"</span>:<span>"white"</span>,<br/><span>"category"</span>:<span>"value"</span>,<br/><span>"code"</span>:<span>{</span><br/><span>"rgba"</span>: [<span>0</span>,<span>0</span>,<span>0</span>,<span>1</span>],<br/><span>"hex"</span>:<span>"#FFF"</span><br/><span>}</span><br/><span>}</span>,<br/><span>{</span><br/><span>"id"</span>:<span>3</span>,<br/><span>"color"</span>:<span>"red"</span>,<br/><span>"category"</span>:<span>"hue"</span>,<br/><span>"type"</span>:<span>"primary"</span>,<br/><span>"code"</span>:<span>{</span><br/><span>"rgba"</span>: [<span>255</span>,<span>0</span>,<span>0</span>,<span>1</span>],<br/><span>"hex"</span>:<span>"#FF0"</span><br/><span>}</span><br/><span>}</span>,<br/><span>{</span><br/><span>"id"</span>:<span>4</span>,<br/><span>"color"</span>:<span>"blue"</span>,<br/><span>"category"</span>:<span>"hue"</span>,<br/><span>"type"</span>:<span>"primary"</span>,<br/><span>"code"</span>:<span>{</span><br/><span>"rgba"</span>: [<span>0</span>,<span>0</span>,<span>255</span>,<span>1</span>],<br/><span>"hex"</span>:<span>"#00F"</span><br/><span>}</span><br/><span>}</span>,<br/><span>{</span><br/><span>"id"</span>:<span>5</span>,<br/><span>"color"</span>:<span>"yellow"</span>,<br/><span>"category"</span>:<span>"hue"</span>,<br/><span>"type"</span>:<span>"primary"</span>,<br/><span>"code"</span>:<span>{</span><br/><span>"rgba"</span>: [<span>255</span>,<span>255</span>,<span>0</span>,<span>1</span>],<br/><span>"hex"</span>:<span>"#FF0"</span><br/><span>}</span><br/><span>}</span>,<br/><span>{</span><br/><span>"id"</span>:<span>6</span>,<br/><span>"color"</span>:<span>"green"</span>,<br/><span>"category"</span>:<span>"hue"</span>,<br/><span>"type"</span>:<span>"secondary"</span>,<br/><span>"code"</span>:<span>{</span><br/><span>"rgba"</span>: [<span>0</span>,<span>255</span>,<span>0</span>,<span>1</span>],<br/><span>"hex"</span>:<span>"#0F0"</span><br/><span>}</span><br/><span>}</span><br/>]<br/><span>}</span></div></div></div></details>

   As soon as you paste the example JSON, the**Character Field**displays the list of colors and the categories.  
   ![image2021-6-7_14-51-53.png](.attachments/Creating-dynamic-selection-lists-for-Progressive-Web-Applications-by-using-JSON-data_image2021-6-7_14-51-53.png)
4. To the**Json Exp**field, add the following expression:  
   colors[id=1].color
5. Click**Extract Value**.  
   The active link uses the expression in the**Json Exp**field and displays**black**in the**Output**field. The value**black**is associated withid=1in the example JSON data.  
   ![image2021-6-7_14-54-20.png](.attachments/Creating-dynamic-selection-lists-for-Progressive-Web-Applications-by-using-JSON-data_image2021-6-7_14-54-20.png)
6. (*Optional*) If you want to validate additional changes you made inDeveloper Studio, you must sync the cache in Mid Tier.
   1. Log in toDeveloper Studioconfiguration.  
      **<*serverName*>:8080/arsys/shared/config/config.jsp**
   2. Click**Sync Cache**.
   3. Refresh the browser to display the updated Progressive View form.

## Results

The**JSON Menu Label**,**JSON Menu Value**, and**JSON Field ID**properties in a character field extract the required data from the JSON data and display that information in a list. The JSONMAP function extracts specific values that you want from the JSON data and displays it in the associated field when you run the active link.

Related topics

[Creating-fields-that-auto-complete-in-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Creating-fields-that-auto-complete-in-Progressive-Web-Applications/)

[Creating-selection-lists-in-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Creating-selection-lists-in-Progressive-Web-Applications/)

[Creating-list-tables-and-setting-selection-mode-by-using-run-processes-in-Progressive-Web-Applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is254/Developing-Progressive-Web-Applications/Creating-list-tables-and-setting-selection-mode-by-using-run-processes-in-Progressive-Web-Applications/)[JSON examples that you can use](https://www.sitepoint.com/colors-json-example/)[Online JSON validator](https://jsonlint.com/?code=)