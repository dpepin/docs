HelixGPT is a generative Artificial Intelligence (AI) capability within Service Management and IT Operations Management. It helps with quicker problem resolution, better collaboration, and increased productivity. For example, HelixGPT administrators can configure HelixGPT to work with DWP to provide users with precise answers to queries. For more information about HelixGPT, its core capabilities, and products that HelixGPT can work with, see[Product overview](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-HelixGPT/helixgpt254/Getting-started/Product-overview/).

HelixGPT delivers reliable and refined results because it generates answers based on the knowledge articles, not from the Internet or the large language model (LLM)'s general knowledge.

HelixGPT supports HKM as a knowledge source.Itdelivers more precise answers to end-user queries based on an automatically determined set of knowledge articles sourced from HKM.

To view the complete list of all supported knowledge sources, see[Adding data sources in HelixGPT](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-HelixGPT/helixgpt254/Setting-up-and-going-live/Adding-data-sources-in-BMC-HelixGPT/).

Related topics

[Leveraging knowledge articles from HKM in other applications](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Getting-started/Use-cases/Leveraging-knowledge-articles-from-BMC-Helix-Knowledge-Management-by-ComAround-in-other-BMC-applications/)

[Integrating with third-party applications by using the REST API](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Integrating-with-third-party-applications-by-using-the-REST-API/)

[Learning about KCS v6 verified HKM](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Getting-started/Use-cases/Learning-about-KCS-v6-verified-BMC-Helix-Knowledge-Management-by-ComAround/)

## Scenario: Configuring HelixGPT to generate answers based on knowledge articles fromHKM

Scenario: Configuring HelixGPT to generate answers based on knowledge articles from HKM

Apex Global usesDWPto enhance self-service for end users by providing them with knowledge articles, products, and services from multiple lines of business such as IT, HR, and Facilities. Apex Global has their knowledge articles inHKM.Allen is an administrator at Apex Global and has enabled theHelixGPTcapabilities for his end users.Allen selectsHKMas aknowledge source forHelixGPT.

Britney, the end user, wants to fix a WiFi issue, so she enters her query inDWP. A summary of the procedure to fix WiFi issues is provided along with the related knowledge article links fromHKM.

Britney follows the procedure and successfully resolves the issue without sifting through a list of knowledge articles to find the relevant one for her query.

## Workflow for configuringHKMas a data source for HelixGPT

The following image shows the process of configuring HKM as a data source for HelixGPT:

![HKM_data_source_GPT.png](.attachments/Leveraging-knowledge-articles-as-a-data-source-for-HelixGPT_HKM_data_source_GPT.png)

| Task<br> | Action<br> | Role<br> | Reference<br> |
| --- | --- | --- | --- |
| 1<br> | Configure HKM as an information source.<br> | The HelixGPT administrator<br> | [Adding data sources in HelixGPT](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-HelixGPT/helixgpt254/Setting-up-and-going-live/Adding-data-sources-in-BMC-HelixGPT/) |
| 2<br> | Ingest data from HKM into HelixGPT.<br> | The HelixGPT administrator<br> | [Ingesting data into HelixGPT](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-HelixGPT/helixgpt254/Setting-up-and-going-live/Ingesting-data-into-BMC-HelixGPT/)<br> |

**Important**

Configuring data sources and ingesting data into HelixGPT are the initial steps to set up HelixGPTto work with applications. For the next steps, see[Setting up and going live](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-HelixGPT/helixgpt254/Setting-up-and-going-live/)and[Administering](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-HelixGPT/helixgpt254/Administering/).

## Result

After the administrator has enabledHelixGPTcapabilities forDWPand selectedHKMas a knowledge source, end users can find answers to their queries from the Catalog, My Activity, or other custom pages created in the Studio. Answers are generated based on automatically determined set of knowledge articles from HKM.

![GPT_HKM.png](.attachments/Leveraging-knowledge-articles-as-a-data-source-for-HelixGPT_GPT_HKM.png)