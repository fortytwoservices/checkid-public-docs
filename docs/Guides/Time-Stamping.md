# Time Stamping

Time stamping is an optional feature that allows for an timestamp to be omitted and written to a custom secrutity attribute everytime an account is claimed via CheckID.

This applies to initial Onboarding and account reset requests handled via CheckID.

## Why Time Stamping?

- Enables Identity Teams to ensure accounts are active
- Enables you to discover "uncliamed accounts" for Security Goverance
- Enables "light" audit log capbility

To give customers insight into if/when a user has used bankid to prove their identity we should write a timestamp to a CSA on the user object in Entra.

Every time a user selects an account on the account selection page, we will update the timestamp attribute with the current time.

The timestamp attribute will be a custom security attribute specified by the customer in a similar format as the entra attribute we use for account matching.
