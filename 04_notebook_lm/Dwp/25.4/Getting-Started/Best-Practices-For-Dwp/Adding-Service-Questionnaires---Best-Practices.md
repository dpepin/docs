As a catalog administrator, you create question forms for users to complete when they submit requests. A questionnaire is a unique question set associated with a service and its workflow. Review the following best practices when adding questionnaires to services.You can also download and use the predefined questionnaires attached to[Leveraging popular service examples to optimize service configurations and enhance user experience](https://docs.bmc.com/xwiki/wiki/internal/view/Service-Management/Employee-Digital-Workplace/dwpMaster2/Creating-and-managing-the-service-catalog/Leveraging-popular-service-examples-to-optimize-service-configurations-and-enhance-user-experience/).

Related topics

[Creating-service-questionnaires](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Creating-and-managing-the-service-catalog/Building-service-catalogs/Creating-service-questionnaires/)

[Leveraging popular service examples to optimize service configurations and enhance user experience](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Creating-and-managing-the-service-catalog/Leveraging-popular-service-examples-to-optimize-service-configurations-and-enhance-user-experience/)

![questionnaire_designer.png](.attachments/Adding-service-questionnaires---best-practices_questionnaire_designer.png)

* Keep a one-to-one mapping between a service and its questionnaire. Associate a questionnaire with only one service, but you can use the same workflow for more than one service.
* Prefill known information or auto-complete answers. Create action triggers to prepopulate question responses with information from ITSM forms. For more information, see[Creating-questions-with-default-responses](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Creating-and-managing-the-service-catalog/Building-service-catalogs/Creating-service-questionnaires/Creating-questions-with-default-responses/).
* Use forms to look up user assets and other data relevant to the request. Build selection menus for question responses where you can pull existing data from the external systems. For more information, see[Creating-selection-menus-for-question-responses](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Creating-and-managing-the-service-catalog/Building-service-catalogs/Creating-service-questionnaires/Creating-selection-menus-for-question-responses/).  
    
  For example, you create a question for a site, and map the selection values to the SIT:Site form; site is a physical location with a mailing address, such as a building. When you complete the question, the settings appear as shown in the following image:  
    
  ![Question_map_to_form.png](.attachments/Adding-service-questionnaires---best-practices_Question_map_to_form.png)
* Keep questions precise and easy to understand. Only ask questions that are necessary.
* Limit the number of questions to ensure good performance in retrieving, saving, and submitting the request.
* Shorten long questionnaires either by reducing the number of questions or by distributing the questions across multiple pages.  
    
  ![Questionnaire_pages.png](.attachments/Adding-service-questionnaires---best-practices_Questionnaire_pages.png)
* If a questionnaire has a question that is a dropdown question based on a form, and that form has a lot of data, we recommend you use a lookup question instead of a dropdown question.
  + When a dropdown list loads for the user requesting the service, it loads all the data in the form. Users need to wait for the data to be downloaded and then for the question to be rendered. However, a lookup list retrieves data only when it is clicked.
  + If the number of records queried by the dropdown list is greater than the value of the**Max-Entries-Per-Query**, the result set is limited to the number of records specified in the**Max-Entries-Per-Query**. It is better to use a lookup question ifthe number of records exceeds**Max-Entries**.
  + When there are a large number of items, it's easier to search through a lookup list for the required data than to scroll through a dropdown list.
* Add indexes on searchable fields when querying custom records.
* When defining questions that result in a query against assets, restrict the results to a specific**Data Set Id**.