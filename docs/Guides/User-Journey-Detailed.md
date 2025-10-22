# User Journey with technical details

## Step 1 - User chooses method of authentication

![Step 1](./media/Step1.png)

## Step 2 - Choose between returning or new hire

Depending on whether the user is a returning employee or a new hire, they choose the appropriate selection.

![Step 2](./media/Step2.png)

## Step 3 - Select account to onboard

A value from the authentication session is used to determine which user accounts the person has. These are shown as a list and the user can choose which account to onboard.

![Step 3](./media/Step3.png)

## Step 4 - Install Microsoft Authenticator

The first step that the user needs to do is to install the Microsoft Authenticator app. Here, the option to the Google Play Store or Apple App store is shown. If the user signs in from another device than their phone, the user can show the QR code in order to navigate with those.

At the same time this step is shown, a [Temporary Access Pass (TAP)](https://learn.microsoft.com/entra/identity/authentication/howto-authentication-temporary-access-pass) is created for the user account. This allows some time for the TAP to be replicated in Entra ID.

![Step 4](./media/Step4.png)

## Step 5 - Sign into Microsoft Authenticator

The user is told to sign into the Microsoft Authenticator app with the userPrincipalName and the generated TAP.

![Step 5](./media/Step5.png)

During this step, when following our [Getting Started guide](../Getting-Started.md), the user will end up with an Authenticator app that both support [notification based MFA](https://learn.microsoft.com/entra/identity/authentication/concept-authentication-authenticator-app#passwordless-sign-in-via-notifications) and [passkey based MFA](https://learn.microsoft.com/entra/identity/authentication/concept-authentication-authenticator-app#passkey-sign-in). They will also be told to register their device, if you have configured this policy.

## Step 5 (OPTIONAL) - Set a password

> NOTE: It is possible to choose whether this step is shown or not. If you do not need passwords, this can be hidden.

The user will be told to click the set password button, and clicking it will open a dialogue where the user sets a password.

![alt text](./media/Group%2050.png)

In the dialogue the user will be prompted to set a password. Note that the user will be able to see whether they meet all the password requirements.

![alt text](./media/Pwd-set-Step.png)

## Step 6 - The process is complete

Once the above steps have been completed, the user is shown a screen that confirms that the account is now set up and optionally a set of useful links and FAQ.

![Step 6](./media/Step6.png)

## So what about the computer?

Signing into the computer is the next step, and the phone is now used for this operation - at least when the computer is Entra Joined. For Entra Joined devices, the [Web sign-in for Windows](https://learn.microsoft.com/windows/security/identity-protection/web-sign-in) is recommended. Here, the user can use the passkey they got in Step 4 for signing passwordlessly into their computer. The computer will then enroll with Windows Hello for Business, which will take over as the users normal method of authentication on that device.

## But we have Macs?

> Note: Documentation not complete yet. We are working on it. In the mean time, have a look at these:

<https://learn.microsoft.com/entra/identity/devices/device-join-microsoft-entra-company-portal?tabs=secure-enclave>

<https://learn.microsoft.com/entra/identity/devices/device-join-macos-platform-single-sign-on?tabs=secure-enclave>
