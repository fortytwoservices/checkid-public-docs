

## Configure Consent and Entra ID Settings

To allow CheckID to function correctly, you'll need to configure a few settings in Microsoft Entra ID.

## Step 1 – Consent to the CheckID Application

As a **Global Administrator**, you need to provide tenant-wide admin consent for the CheckID app.

Visit the following URL to review and approve the necessary permissions:

<https://login.microsoftonline.com/common/adminConsent?client_id=b1c6646a-37c6-4a69-ae96-d6468e2c2a89>

![Consent flow example](image-1.png)

### Permissions requested

| Permission | Why it’s needed |
|------------|------------------|
| [**User.Read.All**](https://learn.microsoft.com/en-us/graph/permissions-reference#userreadall) | Allows CheckID to locate and read user account details in your tenant |
| [**UserAuthenticationMethod.ReadWrite.All**](https://learn.microsoft.com/en-us/graph/permissions-reference#userauthenticationmethodreadwriteall) | Allows CheckID to create a Temporary Access Pass (TAP) for users |
| [**CustomSecAttributeAssignment.Read.All**](https://learn.microsoft.com/en-us/graph/permissions-reference#customsecattributeassignmentreadall) | Enables CheckID to read custom attribute assignments. This permission has no effect unless the CheckID service principal is explicitly assigned the **Attribute assignment reader** role in Microsoft Entra. |

## Step 2 - Configure the recommended Conditional Access policies

> **Note:** This step is only relevant if you have conditional access policies that requires **phishing resistant MFA** or **passwordless MFA** as authentication strength, or requires **app protection policies** or **approved apps** only.

We have several recommended configurations, depending on your situation. There are two "issues" we need to handle during onboarding, which is [app protection](Conditional-Access/Require-Approved-Or-Protected-App-Policy.md) and [authentication strength](Conditional-Access/Authentication-Strength.md). To support the Microsoft recommended approaches, with temporarily exempting the user from certain conditional access policy requirements, CheckID has two features available:

- Automatic maintenance of an Entra ID security group for onboarding users
- Calling a webhook with information about the user doing the onboarding, where the target webhook can do the same thing as the previous feature (adding a person temporary to a group)

## Step 3 - Configure Temporary Access Pass

Our recommended onboarding approach is to have users register the Microsoft Authenticator app using a [Temporary Access Pass](https://learn.microsoft.com/en-us/entra/identity/authentication/howto-authentication-temporary-access-pass), while getting a passkey enrolled at the same time. This means that the feature Temporary Access Pass and Passkey should be enabled in the tenant. 

In the [**Entra portal**](https://entra.microsoft.com/#home), open **Protection** and **Authentication methods**. 

Configure **Passkey (FIDO2)** to **target all users** with the below configuration:

![alt text](image.png)

Configure **Temporary Access Pass** to **target all users** with the below configuration:

![alt text](image-2.png)