### Test for AppliedCustomerBillingRate

Test for AppliedCustomerBillingRate which include 2 custom attributes: `relatedParty` and `lastUpdate`.

#### `1. TrackedShareableEntity.schema.json`

Tests using the *TrackedShareableEntity.schema.json*, which includes other dependencies schema through `allOf`.

- **Use Case 1** - Test creation AppliedCustomerBillingRate with 2 `relatedParty`
    - a `POST` call to create an applied: `OK`
    - a `GET` call to get **ALL** applied (list): `java.lang.IllegalStateException: Expected BEGIN_ARRAY but was BEGIN_OBJECT at path $.relatedParty`
    - a `GET` call to get by **ID** the apply: `OK` (with `2 relatedParty`)
<br>
- **Use Case 2** - Test creation AppliedCustomerBillingRate with 1 `relatedParty`
   - a `POST` call to create an applied: `OK`
   - a `GET` call to get **ALL** applied (list): `java.lang.IllegalStateException: Expected BEGIN_ARRAY but was BEGIN_OBJECT at path $.relatedParty`
   - a `GET` call to get by **ID** the apply: `java.lang.IllegalStateException: Expected BEGIN_ARRAY but was BEGIN_OBJECT at path $.relatedParty`

#### `2. AppliedCustomerBillingRate.schema.json`

Tests using the *AppliedCustomerBillingRate.schema.json*, which includes attributes within `properties`.

- **Use Case 1** - Test creation AppliedCustomerBillingRate with 2 `relatedParty`
    - a `POST` call to create an applied: `OK`
    - a `GET` call to get **ALL** applied (list): `OK` *(but only one relatedParty)*
    - a `GET` call to get by **ID** the apply: `OK` *(with 2 relatedParty)*
<br>
- **Use Case 2** - Test creation AppliedCustomerBillingRate with 1 `relatedParty`
   - a `POST` call to create an applied: `OK`
   - a `GET` call to get **ALL** applied (list): `OK` *(1 relatedParty)*
   - a `GET` call to get by **ID** the apply: `OK` *(1 relatedParty)*
