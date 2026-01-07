The end-user console is a single pane of glass for end users to find knowledge articles, submit service requests, view the status of their requests, and work on action items assigned to them by managers or team leaders.

Single tasks fromBusiness Workflowsthat are assigned to end users by managers or team leaders are called To-dos. To-dos are actions that end users must complete to achieve a common, bigger goal. End users can save time by viewing and completing their To-doswithout moving away from the end user console.

The benefits include:

* Managers or team leaders can assign To-dos to their reportees and colleagues.
* Managers or team leaders can assign a form or questionnaires that require completion by assignees.
* Assignees receive notifications when To-dos are assigned, so that they do not miss them.
* Assignees receive proactive reminders via email as the due date approaches, minimizing the risk of missed deadlines.
* Assignees can mark a To-do as complete only after they have answered all the mandatory questions, if any.
* Assignees can save and close the To-dos questionnaire at any time and revisit it later to complete the task.
* Assigners can monitor the progress of assigned To-dos by tracking when end users mark them as complete.
* Assigners and assignees can communicate with each other via comments to the To-dos.

Required license

[![DWP Advanced icon.png](.attachments/Enabling-end-users-to-work-on-To-dos_DWP-Advanced-icon.png)](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Planning/License-types-and-features/)![DWP external users icon.png](.attachments/Enabling-end-users-to-work-on-To-dos_DWP-external-users-icon.png)DWP and

DWP External users[licenses](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Planning/License-types-and-features/)

Related topic

[Use-cases](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Getting-started/Use-cases/)

## Scenario: Viewing and completing end user assignments by using To-dos

Scenario

Sarah is a new employee being onboarded to Apex Global. She is a self-registered, external user ofDWP. Bill is the hiring manager who assigns To-dosto her as part of her onboarding process.

![How to-dos work.png](.attachments/Enabling-end-users-to-work-on-To-dos_How-to-dos-work.png)

After submitting a To-do, the end user in DWP*cannot*reopen the To-do. Agents inBusiness Workflowscan reopen a To-do and reassign it to the end user.

## Scenario: Displaying To-dos in a studio page

As an administrator, you can add and configure the To-Dos event type in studio pages.

Scenario

Apex Global uses the studio capability to create a custom home page for the end users. Allen, the administrator, wants to make sure that Britney, an end user, can view the To-dos assigned to her.

* Allen configures the To-do event type in the studio page and makes the studio page available for Britney.
* Allen enables the To-do capability for end users.
* Bill, who is Britney's manager, assigns To-dos to Britney to complete two mandatory training sessions and adds the due date.
* Britney views the To-dos and marks them complete after taking the mandatory trainings.
* Bill sees that Britney has completed the To-dos.

## Scenario: Searching for To-dos in HelixGPT

After an administrator has configured HelixGPTwith DWP, end users can search for To-dos in HelixGPT*.*

Scenario

Britney is a new employee being onboarded to Apex Global. She was assigned the following To-dos as part of her onboarding process:

* Passport and visa documents
* Candidate photograph
* Educational documents

During her onboarding, Britney needs to focus on multiple different activities. So, she wants to make sure that she completes all her assigned To-dos on time. Instead of looking for each assigned To-do separately, she searches for*Show my current To-dos*in theHelixGPTchat bar to see the list of all her assignments.

For more information about searching for To-dos in HelixGPT, see[Using-Employee-Navigator-to-find-AI-generated-answers](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Using-BMC-Helix-Digital-Workplace-to-request-services/Using-Employee-Navigator-to-find-AI-generated-answers/).

## Configuring the To-dos workflow

The following image shows the workflow of To-dos associated with a case inBusiness Workflowsand assigned to an end user in DWP:

![Workflow_To-dos in DWP.png](.attachments/Enabling-end-users-to-work-on-To-dos_Workflow_To-dos-in-DWP.png)

| Product<br> | User<br> | Action<br> | Reference<br> |
| --- | --- | --- | --- |
| Business Workflows<br> | Case Business Analyst<br> | * Defines a new template for To-dos. * Defines a task flow for To-dos. | [To dos](https://docs.bmc.com/xwiki/bin/view/Service-Management/Enterprise-Service-Management/BMC-Helix-Business-Workflows/bwf251/Getting-started/Key-concepts/Task-Management/To-dos/)<br> |
| DWP Catalog<br> | Case Business Analyst with catalog administrator permissions<br> | * Creates the Task type action to display the questionnaire for the end user (To-do assignee). * Creates a workflow to update the To-dos status and display the end user's answers inBusiness Workflows. * Creates a To-do questionnaire, which is presented to the end users when the To-dos is assigned. | * [To create a service action](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Creating-and-managing-the-service-catalog/Building-service-catalogs/Managing-service-actions/#Managingserviceactions-Createserviceaction) * [Designing-a-workflow-to-update-To-dos-in-Business-Workflows](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Creating-and-managing-the-service-catalog/Building-service-catalogs/Workflows-for-service-fulfillment/Designing-a-workflow-to-update-To-dos-in-BMC-Helix-Business-Workflows/) * [Creating-questionnaires-for-To-dos](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Creating-and-managing-the-service-catalog/Building-service-catalogs/Creating-service-questionnaires/Creating-questionnaires-for-To-dos/) |
| DWP<br> | Administrator<br> | * Enables To-dos for end users and specify whether you want to display the priority of To-Dos. * *(Optional)*If you want to display To-dos for end users in a custom page,configures the To-do event in the relevant studio page. Ensure that you make the studio page available to end users and add it to the navigation menu. | * [Enabling-end-user-features](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Administering/Administering-BMC-Helix-Digital-Workplace/Managing-end-user-features/Enabling-end-user-features/) * [Creating-pages-in-the-studio](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Administering/Administering-BMC-Helix-Digital-Workplace/Creating-workplaces-for-your-lines-of-business/Creating-pages-in-the-studio/) * [Making-studio-pages-available-to-end-users](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Administering/Administering-BMC-Helix-Digital-Workplace/Creating-workplaces-for-your-lines-of-business/Making-studio-pages-available-to-end-users/) |
| Business Workflows<br> | Case Agent<br> | * Associates the appropriate To-do template with the case. * Adds To-dos to the task flow. | [Updating tasks and tracking progress](https://docs.bmc.com/xwiki/bin/view/Service-Management/Enterprise-Service-Management/BMC-Helix-Business-Workflows/bwf251/Working-on-cases-and-tasks/Creating-and-managing-tasks/Updating-tasks-and-tracking-progress/)<br> |
| DWP<br> | End user<br> | * Works on and submits the assigned To-dos. | [Working-with-To-dos](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Using-BMC-Helix-Digital-Workplace-to-request-services/Working-with-To-dos/)<br> |