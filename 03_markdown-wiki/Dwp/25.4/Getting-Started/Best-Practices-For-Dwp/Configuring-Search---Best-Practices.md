Search helps end users find correct, structured, and useful information at the correct time and place. Search in DWP can be configured to provide results relevant to the user's intent.We recommend that you review the following best practices when configuring search in the application.

Related topics

[Search-in-DWP](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Getting-started/Key-concepts/Search-in-BMC-Helix-Digital-Workplace/)

[Configuring-search](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Administering/Administering-BMC-Helix-Digital-Workplace/Configuring-search/)

End users can also use HelixGPT to find answers to their queries through the global search bar on the Catalog, My Activity, or other custom pages created in the Studio. The generative AI retrieval processgenerates answers to queries instead of providing a list of knowledge articles.For more information, see[Using-Employee-Navigator-to-find-AI-generated-answers](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Using-BMC-Helix-Digital-Workplace-to-request-services/Using-Employee-Navigator-to-find-AI-generated-answers/).

## Personas

Identify your user personasand tailor the user experience to fit their regional, cultural, and language preferences, as well as accessibility requirements. Learn about your audience's needs, how they search, theirpreferred words, and images, and what will help them get their job done.Structure your service catalog to address the distinct needs of different employee groups. Different roles within the organization, like admin, sales, and tech teams, might need very different IT services. Make sure each role gets the correct services they need for their job.If you have a diverse DWP, think about creating dedicated studio pageswith limited search options.

### Scenario: Different service catalog views

Scenario

Britney, a salesperson, is assisting a customer with their purchase. She notices that the billing software is acting up. She wants to report the issue to the IT department to get it resolved immediately. She logs in to the end-user portal and accesses the service catalog, which is designed specifically for employees like her. The interface is straightforward, with prominent options for reporting technical issues, accessing FAQs for common troubleshooting,mobile applications for on-the-go access,and inventory management software. Britney selects the option to report a technical issue, fills out a simple form, and submits the request.

Meanwhile, Sarah, the marketing manager, accesses the same service catalog but views a different catalog tailored to her role. The catalog is more comprehensive, offering a range of options related todigital marketing platforms, analytics tools, marketing automation tools, social media management platforms, and campaign tracking software.

For a salesperson like Britney, the IT service catalog UI is streamlined and focused on addressing immediate technical issues. For a marketing manager like Sarah, the service catalog caters to her needs for requesting new solutions or features to support strategic initiatives and marketing campaigns.

## Taxonomy

Enhance the searchability and navigation of your catalog by properly categorizing and organizing knowledge articles and catalog items.Tailor the taxonomy to suit specific regions, cultures, languages, and other relevant factors.

### Scenario: Service catalog taxonomy for employees across geographies

Scenario

Britney, transferred to a new office location, discovers that her previous hardware is incompatible in her new work environment. In response to Britney's issue, Hannah, the catalog manager, recognizes the need for an IT service catalog that accounts for regional and cultural differences and creates a bespoke service catalog. Understanding the importance of easy navigation and relevance to diverse contexts, Hannah restructures the catalog to cater specifically to the unique requirements of each geographic location, taking into account regional technology preferences, software usage patterns, and IT infrastructure variations. For example, the service catalog now has hardware options compatible with regional standards, such as voltage requirements or language-specific keyboard layouts, ensuring employees have the appropriate devices for their location.

## Catalog profile optimization

* Use accurate comprehensive content in the**Title**,**Description**, and**Tags**fields of a catalog profile.These are primary search fields. Good content in these fields ensures effective catalog searches.

<details class="confluence-expand-macro panel panel-default"><summary><span class="panel-title"><span class="title-text">Catalog service profile fields</span></span></summary><div class="panel-body"><p><img alt="Catalog service profile fields" data-xwiki-image-style-border="true" height="499" src="../.attachments/Configuring-search---best-practices_catalog_service_fields.png" title="Catalog service profile fields" width="1052"/></p></div></details>

* Use a uniform tagging system for all your catalog items and add keywords in the**Tags**field.
* Use meaningful icons in the logo field to represent services effectively.  
    
  ![service_icons.png](.attachments/Configuring-search---best-practices_service_icons.png)

## Number of results returned by search

Do not overwhelm users with too many results.

* **AND logic**—Enable the AND logic setting if you want to narrow the search. The AND logic will return items that match all search terms.DWP Catalogitems are searched using AND logic, whereas Service Request Management items are searched by using OR logic to match keywords.
* **Effective use of search sources**—Minimize the number of search sources to streamline the search and narrow down the results. You can make it easier for users to find relevant information by designing studio pages with a narrower search scope. For theHKMsource, use filters that utilize article tags toprovide even more precise search results.
* **Wildcards**—Enable wildcards to accommodate spelling variations that might affect search results. This feature helps users to search using alternate spellings and variations of a term and get more comprehensive search results. You can enable wildcard search forDWP Catalogitems. In DWP,global search supports*Begins with*searches, recognizing both complete words and partial ones. For example, a search for printer-related documents displays relevant results even with just "pri" entered. By default, search-related settings for pluggable providers are disabled to prevent interference with full-text search, language-specific tokenization, stemming, and relevance logic.Not all sources support searching with wildcards.

  **Important**

  Leading wildcards are not supported if the search is performed on fields that are indexed for Full Text Search (FTS). Only trailing wildcards are supported for these fields.For more information about wildcards, see[How search with wildcards works](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Getting-started/Key-concepts/Search-in-BMC-Helix-Digital-Workplace/#SearchinBMCHelixDigitalWorkplace-wildcards).
* **Date Filter**–The Global Search in ITSM searches for the DWPC requests according to the value in the**default submitted date filter in days**field. Use this field to list only the results submitted within the specified number of days, back from today.  
  We recommend that you set this value to 90. To disable this filter, set this value to 0.

## Knowledge base

* Maintain a quality knowledge base. A well-maintained knowledge base is highly effective in quick and low effort task completion.
* Create content that matches the users' needs and vocabulary, taking into account regional, cultural, and linguistic differences.
* Make sure that knowledge articles are tagged consistently.
* Configure filters to use tags that provide geo-based, company-based, or other specific search results.
* Personalize the content to specific contexts as needed, by creating variants of an article. Cultural variants might include examples, references, or illustrationsrelevant to diverse user backgrounds.Article variants can also accommodate varying user roles, skill levels, or preferences, offering personalized guidance and support.
* Implement a strict process to maintain the articles best supported byHKM.
* Consider prioritizing automated catalog items or the knowledge base based on your needs. Enable the**Natural language searching**setting to facilitate the distinction between catalog items and knowledge articles. This feature enables the search engine to comprehend the context of a sentence or phrase, discern the user's intent, and deliver relevant results accordingly.

## Search bar configuration

Add search bars in your studio pages to allow users to find things on their own and resolve their issues without the need to raise help-desk tickets or to contact support. Make sure the search bar is prominently positioned at the top of studio pages, accompanied by a search icon, and sized appropriately to accommodate typical search queries. Use variables to personalize the search bar text based on the user initiating the search, enhancing the user experience.

## Catalog and knowledge base cleanup

Periodically review catalog items and knowledge articles for usage. Remove or unpublish unused items.

## Permissions for users

Make sure that only users with the correct permissions canaccess articles and services displayed in search results. Hide pages from users who lack the requisite permissions to view them.

## Feedback

Use satisfaction surveys to collect information about your users to improve their search experience.

## customer success webinar

Watch the following webinar to learn how to improve search in DWP.

[🎥 Watch Video: https://www.youtube.com/watch?v=SB022vFsKgY](https://www.youtube.com/watch?v=SB022vFsKgY)

![icon_play@2x.png](.attachments/Configuring-search---best-practices_icon_play%402x.png)[Webinar: How To Improve Search In DWP](https://www.youtube.com/embed/SB022vFsKgY)