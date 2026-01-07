HKMis a subscription-based service that provides a centralized system to create, search, and access knowledge across multiple cloud data sources.

Related topics

[User interface overview](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Getting-started/User-interface-overview/)

[Setting up and going live](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Setting-up-and-going-live/)

[HKM service](https://docs.bmc.com/xwiki/bin/view/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/BMC-Helix-services/BMC-Helix-Knowledge-Management-by-ComAround-service/)in the Subscriber documentation.

The following diagram gives an overview of the HKM architecture:

![CA_architecture_23.3.02.png](.attachments/HKM-architecture_CA_architecture_23.3.02.png)

The components in a typical HKM system are described below:

* + - [HKM web platforms](#Hwebplatforms)
    - [Microsoft Azure Services](#HMicrosoftAzureServices)
    - [Third-party dependencies](#HThird-partydependencies)
    - [Sizing considerations](#HSizingconsiderations)

### HKM web platforms

The following web platforms are used by knowledge workers and end users:

| Component<br> | Description<br> |
| --- | --- |
| HKM Self-Service<br> | Web platform for consumption of knowledge for the end users. The platform is designed to make knowledge articles easy to find and easy to read.<br> |
| HKM Knowledge<br> | Web platform for knowledge workers that includes all the capabilities of HKM. This platform is used to create, maintain, and share knowledge as well as configure the administration settings for your company.<br> |
| HKM Knowledge vNext<br> | Web platform for knowledge workers that includes the decision tree capability. This platform is used to create, maintain, and share knowledge.<br> |

### Microsoft Azure Services

The following key Microsoft Azure services are used for cognitive search, data storage, and reporting insights:

| Component<br> | Description<br> |
| --- | --- |
| Azure Application Service<br> | Hosts web applications and backend functions.<br> |
| Azure Storage Service<br> | Stores files in a geo-redundant storage account (GRS), and data is replicated to a secondary region to ensure durability and high availability.<br>This service includes the following products:<br>  * Azure SQL Database Premium—Stores users, portals, and content. * Azure Blob Storage—Hosts images, videos, and attachments to knowledge articles. |
| Azure Cognitive Search<br> | Powers the AI search capabilities in HKM.<br> |
| Power BI<br> | Provides data and insights in HKM.<br> |
| Azure Analysis Services<br> | Extracts data from HKM as an insight connector.<br> |
| Azure API Management<br> | Handles all API calls and creates API subsets.<br> |

### Third-party dependencies

The following third-party applications are used to enhance the knowledge workers' experience:

| Component<br> | Description<br> |
| --- | --- |
| Froala Content Editor<br> | Enables knowledge workers to create and edit knowledge articles in HKM.<br> |
| Google Translation Service (Optional)<br> | Translates knowledge articles in HKM.<br> |
| Sendgrid (Optional)<br> | Handles email communication in HKM.<br> |

### Sizing considerations

When knowledge workers create content in HKM, they must consider the following types of content size limitations:

* [Article size limitations](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Getting-started/BMC-Helix-Knowledge-Management-by-ComAround-architecture/#article_size)—These limitations apply to the article size and character count.
* [Field-specific limitations](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Knowledge-Management-by-ComAround/hkm/Getting-started/BMC-Helix-Knowledge-Management-by-ComAround-architecture/#field_size)—These limitations apply to individual fields in articles, folders, and links.

#### Article size limitations

When knowledge workers create articles, they must consider limitations related to article size and character count. These limitations affect the ability to save articles, use machine translation, and access version history.

**Important**  
These limitations apply per individual language version of an article. If the article is available in multiple languages, the limitations apply to each translation separately.

| Category | Limit (per single language version) | Impact if exceeded | Details |
| --- | --- | --- | --- |
| Article size | 1 MB | The article can't be saved. | The size of an article is calculated based on its text and formatting. Images and attachments are excluded from this calculation because they are stored separately.<br>The actual size depends on character type and formatting, not the character count. For example, Chinese characters might consume more bytes than English characters. As a result, fewer Chinese characters can fit within the 1 MB limit.<br> |
| A single image or attachment must not exceed 350 MB. |
| The combined size of all translations can exceed 1 MB, but each language version must remain within the 1 MB limit. For example, if an article is available in English, Swedish, and German, its total size can exceed 1 MB. |
| Machine translation | 30,000 English characters | Machine translation is unavailable.<br> | The limit applies to the total number of characters across all fields in an article.<br>If exceeded, machine translation is unavailable, but manual translation remains possible.<br> |
| Version history | 31,940 English characters | The article can be saved, but it doesn't appear in the article history.<br> | The limit applies to the total number of characters across all fields in an article.<br>If exceeded, the article can be saved, but it is not included in the article history. As a result, version management is unavailable for this article version, and it can't be restored or refactored later on.<br> |

**Important**  
The limit is measured in English characters. For other languages, the threshold may vary due to differences in character encoding.

#### Field-specific limitations

The following table lists character limits for specific fields in articles, folders, and links. If any of these limits are exceeded, the item cannot be saved. This rule applies even when other content size limits are within acceptable ranges. For example, if an article title is longer than 2,000 characters, the article cannot be saved. This restriction applies even when the total size of the article is within acceptable limits.

| Item | Field | Limit (English characters) |
| --- | --- | --- |
| **Articles** | Title | 2,000 |
| Author Email | 2,000 |
| Author | 2,000 |
| External links | 128 |
| **Folders** | Title | 2,000 |
| Author Email | 2,000 |
| Description | 2,000 |
| Author | 2,000 |
| External links | 128 |
| **Links** | Title | 2,000 |
| Author Email | 2,000 |
| URL | 2,000 |
| Author | 2,000 |
| External links | 128 |

**Important**  
The limit is measured in English characters. For other languages, the threshold may vary due to differences in character encoding.