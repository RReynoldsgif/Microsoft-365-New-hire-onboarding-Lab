# Microsoft-365-New-hire-onboarding-Lab

# Microsoft 365 New Hire Onboarding Lab

## Overview

In this lab, I completed a new employee onboarding request for the fictional company HorizonTech using Microsoft 365 and Microsoft Entra ID.

The goal was to provision a new Finance employee with a Microsoft 365 account, appropriate licensing, department-based group membership, multi-factor authentication, and access to company cloud services.

## Scenario

HorizonTech hired a new Finance Analyst who needed their account configured before their first day.

### New Employee

- Name: Jordan Lee
- Job Title: Finance Analyst
- Department: Finance
- Company: HorizonTech
- Employee ID: FIN-1001
- Account Type: Standard User

## Technologies Used

- Microsoft 365 Admin Center
- Microsoft Entra ID
- Microsoft 365 Business Premium
- Microsoft Authenticator
- Outlook Web
- OneDrive
- SharePoint Online
- Microsoft Teams
- Entra Sign-In Logs

## Onboarding Process

### 1. Created the Employee Account

Created Jordan Lee as a new Microsoft 365 user in the HorizonTech tenant.

Configured the employee's username, display name, job title, department, company information, and employee ID.

![New User Account](screenshots/01-new-user-account.png)

### 2. Assigned Microsoft 365 Business Premium

Assigned the Microsoft 365 Business Premium license to provide access to Microsoft 365 services including Outlook, OneDrive, SharePoint, and Teams.

![Microsoft 365 License](screenshots/02-m365-license.png)

### 3. Assigned Department Group Membership

Added Jordan Lee to the Finance-Users security group in Microsoft Entra ID.

Using security groups allows HorizonTech to manage department-based access without configuring permissions individually for every employee.

![Finance Group Membership](screenshots/03-finance-group.png)

### 4. Verified Least-Privilege Access

Verified that Jordan Lee was configured as a standard employee account with no administrative roles assigned.

This follows the principle of least privilege by providing only the permissions required for the employee's job responsibilities.

### 5. Configured Multi-Factor Authentication

Completed Microsoft Authenticator registration for the employee during the initial sign-in process.

MFA provides an additional layer of account security beyond the employee's password.

### 6. Tested Microsoft 365 Access

Verified successful authentication and access to Microsoft 365 services.

Testing included:

- Outlook Web
- OneDrive
- SharePoint Online
- Office Home
- Microsoft Teams Web Client

### 7. Reviewed Microsoft Entra Sign-In Logs

Reviewed Jordan Lee's Microsoft Entra sign-in activity to verify successful authentication to Microsoft 365 services.

Successful sign-in events were recorded for Outlook Web, SharePoint Online, Office, and Microsoft Teams Web Client.

![Successful Sign-Ins](screenshots/04-sign-in-logs.png)

## Troubleshooting

During testing, Microsoft Teams initially appeared to remain on an Authentication v2 browser page.

I reviewed Microsoft Entra sign-in logs and confirmed that authentication to the Microsoft Teams Web Client was successful.

Because other Microsoft 365 services were functioning and Entra recorded a successful Teams authentication, the issue was isolated to the browser/client loading process rather than the user's identity, MFA configuration, or license.

## Ticket Resolution

New employee Jordan Lee was successfully provisioned for HorizonTech.

The employee account was created, licensed with Microsoft 365 Business Premium, assigned to the Finance security group, configured with Microsoft Authenticator MFA, and verified for Microsoft 365 service authentication.

The account was configured as a standard user with no administrative privileges.

### Status
