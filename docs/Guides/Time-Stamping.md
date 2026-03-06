# Time Stamping

Time stamping is an optional feature that allows for a timestamp to be emitted and written to a custom security attribute every time an account is claimed via CheckID.

This applies to initial Onboarding and account reset requests handled via CheckID.

## Why Time Stamping?

- Enables Identity Teams to ensure accounts are active
- Enables you to discover "unclaimed accounts" for Security Governance
- Enables "light" audit log capability

To give customers insight into if/when a user has used BankID to prove their identity we should write a timestamp to a CSA on the user object in Entra.

Every time a user selects an account on the account selection page, we will update the timestamp attribute with the current time.

The timestamp attribute will be a custom security attribute specified by the customer in a similar format as the Entra attribute we use for account matching.
