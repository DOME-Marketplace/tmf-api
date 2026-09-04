## List of Schemas for custom attributes

Here is the list of schemas to use, based on the custom attributes you need in the Entity.

|    |    Schema              |     Attributes                         | TMF Entity               | Reason                 |
|:--:|------------------------|----------------------------------------|--------------------------|------------------------|
| 1  | ExternallyBilled       | relatedParty + pricingLogicalAlgorithm |  ProductOffering (TMF620)| - _relatedParty_: to secure and restrict transmission between involved parties. <br> - _pricingLogicalAlgorithm_:  to define the endpoint of an external Billing Engine. |
| 2  | ShareableEntity        | relatedParty                           | Category (TMF620) <br> ProductOffering (TMF620) <br> ProductOfferingPrice (TMF620)| - _relatedParty_: to secure and restrict transmission between involved parties. |
| 3  | TrackedEntity          | lastUpdate                             |   Individual (TMF632) <br> Organization (TMF632) <br> Product (TMF637) <br> Usage (TMF635) | -_lastUpdate_: to define the date and time of the last update. This attribute is needed for replication. |                     
| 4  | TrackedShareableEntity | relatedParty + lastUpdate              |  AppliedCustomerBillingRate (TMF678)  |  - _relatedParty_: to secure and restrict transmission between involved parties. <br> -_lastUpdate_: to define the date and time of the last update. This attribute is needed for replication.|
| 5  | PriceComponent         | relatedParty + usageSpecId             |  ProductOfferingPrice (TMF620) | - _relatedParty_: to secure and restrict transmission between involved parties. <br> - _usageSpecId_:  to define the identifier of the UsageSpecification (TMF635) |.                      |

Please use the **raw data schema.json**, e.g. for relatedParty set as schema: https://raw.githubusercontent.com/DOME-Marketplace/tmf-api/refs/heads/main/DOME/ShareableEntity.schema.json.

> [!IMPORTANT]
> The TMForum of Access-Node doesn't support the **allOf** feature to include multiple attributes. Any Schemas in the table have the list of attributes in the `properties` field.
