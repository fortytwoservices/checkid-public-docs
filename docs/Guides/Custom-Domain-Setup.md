# Custom Domain Setup

If you'd like to use your own domain with CheckID (e.g. `onboarding.yourcompany.com`), you can do so by setting up a simple DNS record.

## Steps

1. Go to your DNS provider’s control panel.
2. Create a **CNAME** record for the subdomain you want to use  
   *(e.g. `onboarding.yourcompany.com`)*
3. Point the CNAME to your CheckID domain:  
   **`companyname.checkid.no`**

## Example

| Type  | Host / Name             | Points to                |
|-------|-------------------------|--------------------------|
| CNAME | `onboarding`            | `companyname.checkid.no` |

This will make `onboarding.yourcompany.com` serve your CheckID instance.

## Notes

- SSL is automatically provisioned and managed by CheckID. No additional setup is needed on your end.
- Not all CheckID licenses include support for custom domains.  
  Please refer to our website to see which features are included in your plan.
