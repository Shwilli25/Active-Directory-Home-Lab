# Active Directory Administration & User Access Lab

## Project Overview

This project documents my hands-on practice administering a Microsoft Active Directory environment in a virtualized home lab.

I built the environment using Windows Server 2022 and Windows client systems to practice common tasks that an IT Support or junior systems administrator may encounter when supporting users in a Windows domain environment.

Rather than focusing only on creating users, I used the lab to practice how Active Directory connects users, computers, groups, policies, permissions, and shared resources. I also documented troubleshooting situations I encountered while building and maintaining the environment.

> **Note:** This is a personal home lab created for hands-on learning and does not represent professional production experience.

## Lab Environment

- Windows Server 2022
- Windows 10
- Active Directory Domain Services (AD DS)
- Active Directory Users and Computers (ADUC)
- Group Policy Management
- DNS
- NTFS and Share Permissions
- Oracle VirtualBox
- Windows File Explorer

**Domain:** `lab.local`

## Skills Practiced

- Active Directory user and group administration
- Organizational Unit (OU) management
- Security group membership
- Group Policy configuration
- Windows domain joins
- DNS troubleshooting
- Shared folder administration
- Share and NTFS permissions
- Group-based resource access
- User lifecycle management
- Account disabling
- Troubleshooting and verification

## Featured Scenarios

### 1. Windows Client Domain Join & Troubleshooting

Configured a Windows client to communicate with the domain controller and joined the computer to the `lab.local` Active Directory domain.

During my Active Directory lab work, I also encountered connectivity and DNS-related issues involving the virtual network adapters. Troubleshooting these issues helped reinforce the importance of DNS configuration and reliable communication between domain clients and domain controllers.

**Skills practiced:** Domain joins, DNS, Windows networking, client/server connectivity, troubleshooting

---

### 2. Department Shared Folder & Permissions

Created a Finance department structure with users and a security group, configured a shared departmental folder, and applied both Share and NTFS permissions.

Tested access from a domain client to verify that the configured group membership and permissions allowed the intended users to access the shared resource.

**Skills practiced:** Security groups, shared folders, Share permissions, NTFS permissions, group-based access

---

### 3. Group Policy – Control Panel Restriction

Created and configured a Group Policy Object (GPO) that restricted access to Control Panel and PC settings for users within the HR Organizational Unit.

Linked the GPO to the appropriate OU, applied the policy, and verified that the restriction took effect.

**Skills practiced:** Group Policy Management, Organizational Units, policy configuration, policy scope, verification

---

### 4. User Lifecycle Management

Practiced managing an employee account through several stages of the identity lifecycle.

Created the user in the appropriate department, assigned group membership, updated the account when the employee changed departments, removed outdated group membership, assigned the appropriate new membership, and later disabled and moved the account as part of an offboarding scenario.

**Skills practiced:** User administration, group membership, department transfers, access changes, account disabling, identity lifecycle concepts

## Troubleshooting Highlight

One of the most valuable parts of building this environment was troubleshooting an Active Directory/DNS issue after adding an additional NAT network adapter to the domain controller for internet connectivity.

The additional adapter registered its address in DNS, which contributed to unreliable Active Directory communication.

I reviewed the network adapter's advanced DNS configuration and disabled **Register this connection's addresses in DNS** for the adapter that should not have been registering with the domain's DNS service.

After making the change, I verified DNS and domain controller connectivity, internet connectivity, and Active Directory functionality.

This experience helped reinforce an important Active Directory concept:

> **DNS configuration is critical to reliable domain communication.**

## What I Learned

Building this lab helped me understand Active Directory as more than a tool for creating user accounts.

I gained hands-on practice with how users, groups, Organizational Units, Group Policy, DNS, domain-joined computers, and file permissions work together in a Windows domain environment.

The troubleshooting portions were especially valuable because they required me to investigate why something was not working, make a targeted configuration change, and verify functionality afterward.

## Repository Structure

Each featured scenario contains documentation and selected screenshots showing the configuration, testing, and results.

This repository will continue to be refined as I build additional Windows Server and Active Directory administration skills.
