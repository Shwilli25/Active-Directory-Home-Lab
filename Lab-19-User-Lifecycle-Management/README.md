# Active Directory User Lifecycle Management

## Overview

This lab demonstrates the management of a user account through multiple stages of the employee lifecycle in a Windows Server Active Directory environment.

Using a fictional employee, Sophia Turner, I practiced creating an account, assigning department group membership, updating access after a department transfer, disabling the account, and organizing the disabled account into a dedicated Organizational Unit (OU).

> **Note:** This is a personal home lab created for hands-on learning and does not represent professional production experience.

## Lab Environment

- Windows Server 2022
- Active Directory Domain Services (AD DS)
- Active Directory Users and Computers (ADUC)
- Domain: `lab.local`
- Organizational Units (OUs)
- Active Directory security groups

## Skills Practiced

- Active Directory user account administration
- Organizational Unit management
- Security group membership management
- Employee joiner, mover, and leaver concepts
- Updating access after a department change
- Removing outdated group membership
- Disabling user accounts
- Organizing disabled accounts

## Scenario

Sophia Turner was created as a new Finance employee. During the lab, her account progressed through several lifecycle stages:

1. Created as a Finance user
2. Added to the `Finance_Employees` security group
3. Transferred from Finance to HR
4. Removed from the `Finance_Employees` group
5. Added to the appropriate HR group
6. Disabled as part of the simulated offboarding process
7. Moved to a dedicated `Disabled_Users` OU

The screenshots below highlight the most important stages of this process.

## 1. Create the Finance Employee

Sophia Turner's user account was created within the Finance OU.

![Sophia Turner created in Finance](Screenshots/Lab19_Shot2_New_Finance_Employee_Created.png)

## 2. Assign Finance Group Membership

Sophia was added to the `Finance_Employees` security group as part of her Finance department configuration.

![Sophia added to Finance Employees](Screenshots/Lab19_Shot3_Sophia_Added_To_Finance_Group.png)

## 3. Update Membership After Department Transfer

After Sophia was transferred from Finance to HR, her previous Finance group membership was removed.

This demonstrates the importance of removing access that is no longer appropriate when an employee changes roles or departments.

![Sophia removed from Finance Employees](Screenshots/Lab19_Shot5_Removed_Sophia's_Finance_Access.png)

Sophia was then assigned to the HR group as part of the department change. This step is described here as part of the lifecycle workflow; the portfolio screenshots were intentionally limited to the strongest evidence rather than documenting every individual click.

## 4. Disable the User Account

As part of the simulated offboarding stage, Sophia's Active Directory account was disabled.

![Sophia account disabled](Screenshots/Lab19_Shot8_Sophia_Account_Disabled.png)

## 5. Organize the Disabled Account

The disabled account was moved into a dedicated `Disabled_Users` OU to separate inactive accounts from active department users.

![Sophia moved to Disabled Users OU](Screenshots/Lab19_Shot12_Sophia_Moved_To_Disabled_Users.png)

## What I Learned

This lab helped me understand that Active Directory account administration involves more than creating and deleting users. An employee's identity and access can change throughout their time with an organization.

When a user changes departments, old group memberships should be reviewed and removed when they are no longer appropriate, while new memberships can be assigned according to the user's new role. During offboarding, disabling the account prevents continued sign-in while keeping the account available for administrative handling.

The lab also reinforced the importance of keeping Active Directory organized so active and inactive accounts can be managed clearly.
