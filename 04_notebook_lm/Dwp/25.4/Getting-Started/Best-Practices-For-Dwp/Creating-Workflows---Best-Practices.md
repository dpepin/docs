As a catalog administrator, you create workflows for service fulfillment. We recommend that you review and implement the following best practices when configuring your service fulfillment workflows.

Related topics

[Workflows-for-service-fulfillment](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Creating-and-managing-the-service-catalog/Building-service-catalogs/Workflows-for-service-fulfillment/)

## Creating workflows

Make sure you refer to common questions such as how to create workflows inDWP Catalog, how to submit a service request usingDWP CatalogREST API, how to simplify string building inDWP Catalog, and so on at[BEST FAQ on DWP Catalog for catalog workflows](https://community.bmc.com/s/article/BEST-FAQ-on-BMC-Helix-Digital-Workplace-Catalog-Workflow).

The following image shows a sample workflow to create an account:  
![Workflow_create_new_account.png](.attachments/Creating-workflows---best-practices_Workflow_create_new_account.png)

* Determine the workflow scenarios including the need for approval, the type of approval required, and the necessary fulfillments such as cases, work orders, and incidents.
* To increase efficiency, simplify, standardize, and minimize the number of workflows. Fewer workflows mean less development effort and less troubleshooting.
* Create generic, reusable workflows. Avoid creating a separate workflow from scratch for every service. When creating a new service, analyze whether an existing generic workflow can be reused.You can use one workflow for many services, but make sure you have a one-to-one mapping between a service and a questionnaire.Leverage the workflows in the IT-content pack. For more information, see[Setting up the IT content pack](https://docs.bmc.com/xwiki/bin/view/Service-Management/IT-Service-Management/BMC-Helix-ITSM/itsm251/Setting-up-and-going-live/Setting-up-the-IT-content-pack/).  
  Learn how to create reusable workflows at[Configurable, reuseable workorder workflow](https://community.bmc.com/s/news/aA33n000000D0ZbCAK/configurable-reuseable-workorder-workflow)on Communities.
* Use templates to set fulfillment values and automation mechanisms to create work orders, cases, and incidents and reduce the reliance on the service desk.
* If service requirements do not match existing workflows, develop new workflows and prioritize their development.
* Identify the tasks in your workflow and create a flowchart.
* Do not overload a workflow with all the logic in one huge workflow. A workflow with many steps takes longer to load in the designer.It may also become difficult to understand how the steps are connected, especially if links between process activities cross. We recommend that you split the logic in another process and use a**Call Activity**element to call this process. For example, when you have exclusive gateways each branch might do the same thing with a few differences. You could add one process that would handle the different use cases, and this process could be used in each branch, with different parameters.

* Use a subprocess to collapse process steps. Splitting your workflow into smaller workflows makes it easier to understand complex workflows. M ove repeated activities into a subprocess. This approach also helps to isolate callbacks thus preventing them from triggering the wrong sequence of the workflow. This can happen if you create two incidents in a row within the same branch of a workflow.
* Use automation wherever possible. For more informaton, see[Automating-service-requests](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Getting-started/Use-cases/Automating-service-requests/).
* When you design a workflow, first create the process inputs. Map each process input to a process question; the question can be answered by the user or have a default value. By using process variables, you can attach the same workflow to different services, and still provide specific information based on the service.
* If you need to reference an output expression from one activity and use it in other activities in a workflow, assign a local variable to the output expression of the activity.
* If a questionnaire, along with the workflow, is imported from the AWS Service Catalog, set all questions to**Required**.
* If a questionnaire is attached to a workflow that uses AWS Marketplace actions, set all questions to**Required**.
* To prevent a failure in a workflow from processing as expected, use an Error Boundary event to identify the workflow path that must be followed to resolve the error.
* If a workflow has an approval step, make sure the approver field is correctly filled in. For example, if a workflow requires manager approval, fill in the manager field in the CTM:People form. If a user doesn't have a manager assigned, such approval requests will fail.
* For future reference and understanding, document all services and workflows:
  + Document each step, including all decision points.
  + Design the workflow diagram to improve readability.
  + Align elements, use the same size for elements, and add labels when workflows branch.

## Testing and troubleshooting workflows

* After you create a workflow, verify that it works correctly. Iterate and test your workflows, identify improvements, and refine the flows accordingly.
* Test a workflow against its business requirement.
* Make sure your workflow passes through the DEV and QA stages before you deploy it to your PROD environment.
* Test your workflowto make sure you can deliver services within the Service Level Agreements (SLAs).
* Check the workflow execution in the service request report. When you open a service to view its details, the**Error Details**tab shows error details if the service request was unsuccessful. Analyze the For more information, see[Reviewing-the-status-of-service-requests](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Creating-and-managing-the-service-catalog/Reviewing-the-status-of-service-requests/). See also managing processes in[IS](https://docs.bmc.com/xwiki/bin/view/Service-Management/Innovation-Suite/BMC-Helix-Innovation-Suite/is251/)documentation.
* Enable and download the process log file. Process logs capture the information and errors that occur in a workflow. Review the log file to Understand how the process flows from the workflow elements, what value a variable has, and other information.  
  Perform the following steps to enable process logs:

* 1. Log in to Mid Tier, as an administrator.
  2. Select**AR System Management Console > AR System Server Group Console**.
  3. Select**Logs > Logs Management**.
  4. Select either**Server**or**Template**to load the required settings.

* 1. Select**All servers**.
  2. Enable**Process.log**.
  3. Click**Apply**.

* To view the process logs, perform the following steps:
  1. Select**Logs > View Logs**.
  2. Select the server for which you want to view the logs.
  3. Select**process.log**from the log file list, and click**Get File**.
  4. Select the file name in the attachment field and click**Save to Disk.**
  5. Select the download directory and save the log file.
  6. Review the contents of the file to troubleshoot the workflow.

## Editing workflows

* If you want to edit a workflow, make a copy of the workflow and edit the copy.This method ensures the in-process requests are not affected by changes you make.
* When you edit workflows, record what you did and why. This information helps others understand the changes you made.

## Importing workflows

* Take a backup from the PROD environment. If you need to roll back, import the old version.
* When importing, select the option to create a new copy instead of overwriting a workflow.

## Connect with Webinar

Watch the following webinar to learn more about common workflow creation use cases and best practices:

[🎥 Watch Video: https://www.youtube.com/watch?v=YzAVY-3IAnE](https://www.youtube.com/watch?v=YzAVY-3IAnE)

![icon_play@2x.png](.attachments/Creating-workflows---best-practices_icon_play%402x.png)[Webinar: DWP Catalog: Common Workflow Creation Use Cases & Best Practices](https://www.youtube.com/embed/YzAVY-3IAnE)

## Support webinar

Watch the following webinar to learn how to create custom workflows:

[🎥 Watch Video: https://www.youtube.com/watch?v=yX4e51I0gOo](https://www.youtube.com/watch?v=yX4e51I0gOo)

![icon_play@2x.png](.attachments/Creating-workflows---best-practices_icon_play%402x.png)[Webinar: A custom workflow example](https://www.youtube.com/embed/yX4e51I0gOo)