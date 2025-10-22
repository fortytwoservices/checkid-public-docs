# Welcome to CheckID

**CheckID** is a secure and user-friendly onboarding solution that simplifies the first-time sign-in experience for new employees in your organization.

Instead of relying on distributing temporary passwords, manual user setup, and IT bottlenecks, CheckID allows users to authenticate themselves using familiar and secure [identity providers that they already use for online banking or similar](Identity-Providers/Overview.md).

Once signed in, users are automatically provided with access to their Microsoft Entra ID account — fast, secure, and fully compliant.

## Key Benefits

- Zero IT stress: No need to manually create and distribute temporary passwords.
- Frictionless for the user: Uses an authentication method they already know
- Secure by design: Integrates natively with  Microsoft Entra ID and follows all best practices for Zero Trust implementation.

## How It Works

1. The new employee goes to `yourorg.checkid.no` (Optional custom domain) on their phone or laptop.
2. They choose their [preferred authentication method](Identity-Providers/Overview.md).
3. After secure authentication, CheckID:
      - Connects to your Microsoft Entra ID tenant
      - Creates a [Temporary Access Pass (TAP)](https://learn.microsoft.com/entra/identity/authentication/howto-authentication-temporary-access-pass)
      - Guides the user in adding the account to Microsoft Authenticator
4. The user can use Microsoft Authenticator to enroll additional devices, such as their PC

---

Read more on [checkid.no](https://checkid.no) - CheckID is developed by [fortytwo.io](https://fortytwo.io)
