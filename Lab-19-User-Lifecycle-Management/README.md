# Lab 19 – User Lifecycle Management in Active Directory

## Objective
The purpose of this lab was to practice managing the full lifecycle of a user account in Active Directory. Tasks included creating a new employee account, assigning group memberships, transferring the employee to a different department, removing old permissions, disabling the account, and organizing disabled accounts into a dedicated Organizational Unit (OU).

---

## Technologies Used
- Windows Server 2022
- Active Directory Users and Computers (ADUC)
- Organizational Units (OUs)
- Security Groups

---

# Step 1 – Create a New Finance User

A new user account for Sophia Turner was created inside the Finance OU. The account was configured with a username and prepared for Finance department access.

### Screenshot
![Shot1](Screenshots/Lab19_Shot1_New_Finance_User_Window.png)

---

# Step 2 – Verify User Creation

The new Finance employee account was successfully created and appeared inside the Finance OU.

### Screenshot
![Shot2](Screenshots/Lab19_Shot2_New_Finance_Employee_Created.png)

---

# Step 3 – Add User to Finance Security Group

Sophia Turner was added to the Finance_Employees security group. This granted her access to Finance department resources through group-based permissions.

Benefits of using security groups:
- Simplifies permission management
- Reduces administrative overhead
- Allows consistent access control across departments

### Screenshot
![Shot3](Screenshots/Lab19_Shot3_Sophia_Added_To_Finance_Group.png)

---

# Step 4 – Move User to HR Department

Sophia Turner was transferred from the Finance OU to the HR OU to simulate a departmental change within the organization.

This demonstrates how administrators can reorganize user accounts as employees change roles.

### Screenshot
![Shot4](Screenshots/Lab19_Shot4_Sophia_Moved_To_HR.png)

---

# Step 5 – Remove Finance Department Access

Sophia Turner was removed from the Finance_Employees security group to revoke access to Finance department resources.

This follows the Principle of Least Privilege by ensuring users only maintain access required for their current role.

### Screenshot
![Shot5](Screenshots/Lab19_Shot5_Removed_Sophia's_Finance_Access.png)

---

# Step 6 – Add User to HR Security Group

Sophia Turner was added to the HR_Employees security group to grant proper HR department permissions and access.

### Screenshot
![Shot6](Screenshots/Lab19_Shot6_Sophia_Added_To_HR_Group.png)

---

# Step 7 – Disable User Account

Sophia Turner’s account was disabled to simulate an employee termination or inactive account scenario.

Disabling accounts:
- Prevents user logins
- Preserves account information
- Maintains audit history
- Helps improve security

### Screenshot
![Shot7](Screenshots/Lab19_Shot7_Sophia_Disabled_Account_Window.png)

### Screenshot
![Shot8](Screenshots/Lab19_Shot8_Sophia_Account_Disabled.png)

---

# Step 8 – Remove User from HR Group

After disabling the account, Sophia Turner was removed from the HR_Employees security group to fully revoke department access.

This prevents disabled accounts from retaining unnecessary permissions.

### Screenshot
![Shot9](Screenshots/Lab19_Shot9_Sophia_Removed_From_HR_Group.png)

---

# Step 9 – Create Disabled Users OU

A new Organizational Unit named Disabled_Users was created to store disabled employee accounts separately from active users.

Benefits of a Disabled Users OU:
- Improves organization
- Simplifies administration
- Helps with account auditing
- Keeps inactive accounts separated from active employees

### Screenshot
![Shot10](Screenshots/Lab19_Shot10_New_OU_Window.png)

### Screenshot
![Shot11](Screenshots/Lab19_Shot11_Disabled_Users_OU_Created.png)

---

# Step 10 – Move Disabled Account to Disabled Users OU

The disabled Sophia Turner account was moved into the Disabled_Users OU.

This demonstrates proper Active Directory account lifecycle management and organizational best practices.

### Screenshot
![Shot12](Screenshots/Lab19_Shot12_Sophia_Moved_To_Disabled_Users.png)

---

# Conclusion

In this lab, Active Directory user lifecycle management tasks were successfully completed. A new employee account was created, assigned permissions through security groups, transferred between departments, disabled, and archived into a dedicated Disabled Users OU.

Key concepts practiced:
- User account creation
- Security group management
- OU organization
- Access revocation
- Principle of Least Privilege
- Disabled account management
- Active Directory administrative best practices

This lab strengthened hands-on experience with real-world Active Directory administration tasks commonly performed by Help Desk, System Administrators, and IAM professionals.
