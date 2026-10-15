# Microsoft 365 New Hire Onboarding Lab

## Overview

In this hands-on Help Desk lab, I completed a new-hire onboarding workflow for **HorizonTech**, a fictional company, using Microsoft 365 and Microsoft Entra ID.

The goal was to provision a Finance employee with a user account, appropriate licensing and group membership, standard-user permissions, multi-factor authentication (MFA), and access to Microsoft 365 cloud services. I also performed a password reset and reviewed sign-in logs to verify authentication.

## Scenario

HorizonTech hired a new Finance Analyst who needed access to company resources before their first day.

| Employee detail | Value |
| --- | --- |
| Name | Jordan Lee |
| Job title | Finance Analyst |
| Department | Finance |
| Company | HorizonTech |
| Employee ID | FIN-1001 (lab scenario) |
| Account type | Standard user (no administrative roles) |

## Technologies Used

- Microsoft 365 Admin Center
- Microsoft Entra ID
- Microsoft 365 Business Premium
- Microsoft Authenticator (MFA)
- Outlook on the web
- OneDrive
- SharePoint Online
- Microsoft Teams Web Client
- Microsoft Entra sign-in logs

## Onboarding Process

### 1. Created the Employee Account

Created Jordan Lee's user account in the HorizonTech Microsoft 365 tenant and configured the employee profile, including the Finance Analyst job title and Finance department. Verified the new account appeared in Microsoft Entra ID as a member user.

<img width="2048" height="1153" alt="01-new-user-account" src="https://github.com/user-attachments/assets/36d43eb7-3250-46ce-b38d-f5d9e30689b2" />

<img width="3815" height="1810" alt="Screenshot 2026-09-29 205804" src="https://github.com/user-attachments/assets/df3204aa-6897-4d3c-b0e5-ce0930a28448" />

### 2. Assigned Microsoft 365 Business Premium

Assigned **Microsoft 365 Business Premium** in the Microsoft 365 Admin Center. Confirmed the license was selected for Jordan Lee under **Licenses and apps**.

<img width="2048" height="926" alt="02-m365-license" src="https://github.com/user-attachments/assets/9d91da9e-f50d-4184-aca2-6e79d0eed173" />

### 3. Added the Employee to the Finance Security Group

Added Jordan Lee to the **Finance** security group in Microsoft Entra ID and verified that the employee appeared in the group's **Direct members** list.

Using security groups helps administrators manage access by department instead of assigning permissions one employee at a time. Actual access to individual resources still depends on the permissions configured for the group.

<img width="3830" height="1822" alt="Screenshot 2026-09-29 215208" src="https://github.com/user-attachments/assets/f14226e3-5b60-426e-bd5c-9544bcda73db" />
<img width="2048" height="971" alt="03-finance-group" src="https://github.com/user-attachments/assets/6101f196-0d41-42cb-ae0f-01f826b50dcf" />

### 4. Verified Least-Privilege Access

Confirmed that the employee was configured as a **standard user** with **zero administrative roles assigned**. This follows the principle of least privilege: users should receive only the access required to perform their jobs.
<img width="2048" height="1281" alt="04-sign-in-logs" src="https://github.com/user-attachments/assets/926559fc-a729-41ab-8704-e04a17b41e43" />


### 5. Reset the Password and Completed First-Time Sign-In

Performed an administrator-initiated password reset for Jordan Lee in Microsoft Entra ID. The admin center confirmed that the password reset succeeded and generated a temporary password.

<img width="2048" height="1281" alt="05-password-reset" src="https://github.com/user-attachments/assets/3f1a0b41-64b3-4d22-9bba-bb0721625fe3" />

Used the temporary password in a simulated employee sign-in, completed the required password change, and continued to Microsoft 365 account security setup.

**Security note:** The temporary password has been redacted from the screenshot and is not included in this repository.


### 6. Registered Microsoft Authenticator MFA

Completed Microsoft Authenticator registration for Jordan Lee during the first-time sign-in process. The setup flow confirmed **Authenticator Added** and indicated that it was the default sign-in method.


<img width="2048" height="1281" alt="06-authenticator-added" src="https://github.com/user-attachments/assets/dd259391-6082-4c00-b2de-4bc6576d66fb" />

MFA helps protect accounts by requiring an additional verification factor beyond the password.


### 7. Tested Microsoft 365 Service Access

Signed in as Jordan Lee and checked access to the employee's Microsoft 365 environment:

- **Outlook on the web:** Opened the mailbox successfully.
- **OneDrive:** Opened the employee's OneDrive homepage successfully.
- **Office Home:** Successful authentication recorded.
- **SharePoint Online:** Successful authentication recorded.
- **Microsoft Teams Web Client:** Successful authentication recorded, although the browser client did not fully load during testing.

<img width="2048" height="1281" alt="07-outlook-access" src="https://github.com/user-attachments/assets/b03d107e-163a-4d62-b4d6-71e87e510877" />

<img width="2048" height="1281" alt="08-onedrive-access" src="https://github.com/user-attachments/assets/3a96dd1e-7646-4f7f-a681-06e1fcc3e1e6" />

### 8. Reviewed Microsoft Entra Sign-In Logs

Reviewed Jordan Lee's interactive sign-in logs in Microsoft Entra ID. Confirmed successful authentication events for **One Outlook Web, Office Home, Office 365 SharePoint Online, and Microsoft Teams Web Client**.

This verified that the account could authenticate to these services. A successful authentication event does **not**, by itself, prove that every application completed loading or that all application features were functional.

<img width="1408" height="881" alt="Screenshot 2026-10-07 at 5 52 07 PM" src="https://github.com/user-attachments/assets/0686a147-2384-43a4-af32-e71fbcd25d79" /><img width="1408" height="881" alt="Screenshot 2026-10-07 at 7 25 52 PM" src="https://github.com/user-attachments/assets/bb2c9a7a-667a-494b-83d5-436aaaced45f" />
<img width="1408" height="881" alt="Screenshot 2026-10-07 at 5 52 59 PM" src="https://github.com/user-attachments/assets/0ac857e0-be9c-4cc4-8b13-a13d7ac1973e" />


## Troubleshooting: Microsoft Teams Browser Loading

**Symptom:** During service testing, Microsoft Teams appeared to remain on an **Authentication V2** browser page rather than fully opening the Teams interface.

**Troubleshooting performed:**

1. Confirmed that Jordan Lee could sign in to other Microsoft 365 services.
2. Opened the user's Microsoft Entra sign-in logs.
3. Found successful Microsoft Teams Web Client authentication events.
4. Documented that authentication succeeded but full Teams browser functionality was not yet verified.

**Finding:** The evidence showed that Microsoft Entra accepted the Teams sign-in. Additional browser/client troubleshooting would be needed to establish why the interface did not finish loading; the sign-in logs alone do not identify the root cause.

## Ticket Resolution

**Status: Core onboarding completed — Teams browser validation pending**

Successfully created and configured Jordan Lee's employee account, assigned Microsoft 365 Business Premium, added the user to the Finance security group, confirmed standard-user permissions, reset the password, completed the first-time password change, and registered Microsoft Authenticator MFA.

Verified Outlook and OneDrive access and reviewed successful sign-in activity for other Microsoft 365 services. Documented the remaining Microsoft Teams browser-loading issue for follow-up.

## Skills Demonstrated

- New-hire onboarding and Microsoft 365 user provisioning
- Microsoft Entra ID user administration
- Microsoft 365 license assignment
- Security group membership management
- Least-privilege access verification
- Password reset and first-time sign-in support
- Microsoft Authenticator MFA registration
- Outlook and OneDrive access testing
- Microsoft Entra sign-in log analysis
- Help Desk troubleshooting and ticket documentation
