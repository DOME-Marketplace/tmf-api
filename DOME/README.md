## List of Schemas for custom attributes

Here is the list of schemas to use, based on the custom attributes you need in the Entity.

|    |    Schema              |     Attributes                         |
|:--:|------------------------|----------------------------------------|
| 1  | ExternallyBilled       | relatedParty + pricingLogicalAlgorithm | 
| 2  | ShareableEntity        | relatedParty                           |
| 3  | TrackedEntity          | lastUpdate                             |
| 4  | TrackedShareableEntity | relatedParty + lastUpdate              |
| 5  | PriceComponent         | relatedParty + usageSpecId             |

Please use the **raw data schema.json**, e.g. for relatedParty set as schema: https://raw.githubusercontent.com/DOME-Marketplace/tmf-api/refs/heads/main/DOME/ShareableEntity.schema.json.

> [!IMPORTANT]
> The TMForum of Access-Node doesn't support the **allOf** feature to include multiple attributes. Any Schemas in the table have the list of attributes in the `properties` field.
