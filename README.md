# Lookups

This repo is a public mirror of our lookups for coverages and other parameters whose values aren't numbers, booleans, or open-text strings -- meant for users of our Quote to Bind API.

Note that the logic for lookups is that the default lookup will have a name like `policyLimitBIPD`, and then there may also be a lookup with “State” appended to that name, like `policyLimitBIPDState`, which, if there is a set of values for a given state, should be used instead of the default lookup.

| File                                                                                                          | Description                                                                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [publicLookups](https://github.com/gobranch/lookups/blob/main/publicLookups.json)                             | Main lookups for coverages and other quote parameters                                                                                                                                       |
| [mortgageLookups](https://github.com/gobranch/lookups/blob/main/mortgageLookups.json)                         | For the `MortgageDetailsInput` type. You're also allowed to use this to implement mortgage lender autocomplete in your own UI.                                                              |
| [enhancedRoofWindstormValues](https://github.com/gobranch/lookups/blob/main/enhancedRoofWindstormValues.json) | Lookups for windstorm-related roof characteristics                                                                                                                                          |
| [insuranceProvidersList](https://github.com/gobranch/lookups/blob/main/insuranceProvidersList.json)           | Available to implement autocomplete / selection for `currentAutoCarrier`                                                                                                                    |
| [securityProviders](https://github.com/gobranch/lookups/blob/main/securityProviders.json)                     | Known security providers and whether they are Branch partners for Branch's connected home discount. These values can be used for the `providerName` field in the `ConnectedHomeInput` type. |

---

**For Branch employees** -- _You do not want to use this repo in your code._

## For Branch Employees:

_Do not use this repo in your code._ The lookups you're looking for are in `packages/lookups` in the main repo.

The files in this folder are **published publicly** for consumers of our quote to bind API to use. Don't put any lookups that are sensitive or should be private in this folder.

If you need to add sensitive lookup data, add it in the `private-lookups` folder of this package and merge it into the lookups object in `index.ts` similar to what's being done right now.

If you update the lookups in this directory, you might also want to copy the files you updated over to the public mirror at https://github.com/gobranch/lookups
