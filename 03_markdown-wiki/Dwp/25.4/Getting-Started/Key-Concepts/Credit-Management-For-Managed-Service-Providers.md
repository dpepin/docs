Services inDWP Catalogcan be free or chargeable. A service is chargeable if it has a defined price. By default, all chargeable services are priced in USD. The currency is set during the installation ofDWP Catalog.

Required license

[![DWP Advanced icon.png](.attachments/Credit-management-for-managed-service-providers_DWP-Advanced-icon.png)](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Planning/License-types-and-features/)[DWP](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Planning/License-types-and-features/)

Related topics

[Enabling-credit-management](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Administering/Administering-BMC-Helix-Digital-Workplace-Catalog/Setting-up-and-managing-a-credit-based-payment-system/Enabling-credit-management/)

[Managing-customers](https://docs.bmc.com/xwiki/bin/view/Service-Management/Employee-Digital-Workplace/BMC-Helix-Digital-Workplace/dwp254/Administering/Administering-BMC-Helix-Digital-Workplace-Catalog/Managing-customers/)

If the Managed Service Provider (MSP) feature is enabled for theDWP Catalog, catalog administrators can configure the global price setting for all services inDWP Catalog. They can change the default currency-based price to the credit-based price.

Warning

Enable this feature only if you performed a fresh installation ofDWP Catalog. Do not enable this feature if you are upgrading from a previous version.

After this feature is enabled, you cannot use the external users feature or create people groups that your end users can add as collaborators.

## Business case overview

A telecommunication company, which is a managed service provider, has deployed the DWP solution in their data center. The company usesDWP Catalogas a system for creating chargeable services for their customers—companies that provide services to end users.

The telecommunication company needs to be able to define their company customers, push services to them, and invite customer administrators. These administrators manage entitlements for the services that a catalog administrator provided to them. Company customers are charged in credits based on consumption of services. Customer administrators can monitor service consumption and the company’s credit consumption. End users can use DWP as a client management console where they request telecom services.

## Credit-based system overview

You can enable the credit based pricing system only if you have enabled the Managed Service Provider (MSP) mode.

For a multi-customer company, a catalog administrator can use a credit system that replaces the traditional currency-based pricing model.

![msp_credit_flow.png](.attachments/Credit-management-for-managed-service-providers_msp_credit_flow.png)

## Credit balance

The catalog administrator defines the credit balance for each customer of the company. For example, the catalog administrator grants 10,000 credits to its customer company. The balance remains positive until the number of credits is more than zero. The credit balance becomes negative when all credits are used and when the credit value is below zero.

## Service requests with credit-based price enabled

When the credit-based system is enabled, all chargeable services are priced in credits instead of USD. The catalog administrator can provide each tenant with only one pricing system, but the credit-based pricing system works only within the MSP customer.