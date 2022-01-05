# Lookups

This repo is a public mirror of our lookups for coverages and other parameters whose values aren't numbers, booleans, or open-text strings -- meant for users of our Quote to Bind API.

Note that the logic for lookups is that the default lookup with have a name like `policyLimitBIPD`, and then there may also be a lookup with “State” appended to that name, like `policyLimitBIPDState`, which, if there is a set of values for a given state, should be used instead of the default lookup.

| File                                                                                                          | Description                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| [publicLookups](https://github.com/gobranch/lookups/blob/main/publicLookups.json)                             | Main lookups for coverages and other quote parameters                                                                          |
| [mortgageLookups](https://github.com/gobranch/lookups/blob/main/mortgageLookups.json)                         | For the `MortgageDetailsInput` type. You're also allowed to use this to implement mortgage lender autocomplete in your own UI. |
| [enhancedRoofWindstormValues](https://github.com/gobranch/lookups/blob/main/enhancedRoofWindstormValues.json) | Lookups for windstorm-related roof characteristics                                                                             |

---

**For Branch employees** -- _You do not want to use this repo in your code._

The lookups you're looking for are in `packages/lookups` in the main repo.
