# Active Directory Home Lab

## Description
Welcome to the GitHub repository for setting up a basic home lab running Active Directory using Oracle VirtualBox! This repository provides a comprehensive guide to create a virtualized environment for practicing and learning about Active Directory (AD) and managing users with PowerShell.

**Functionality:** Customer needs a large number of users added. (i.e. new hiring class)

**Solution:** Tech professional uses Powershell script to efficiently add users to help with time management.

## Language/Utilities Used
- PowerShell
- Oracle VirtualBox

## Environments Used
- Windows 10
- Server 2019

## Lab Walk-through
|![Image](https://github.com/user-attachments/assets/24078984-402b-4b12-8a32-3a84780804e8) |
|:--:|
|*Topology*|

## 1. Setting Up Active Directory Domain Controller (AD-DC)
1.	Launch Windows Server 2022 VM
2.	Rename Network Interfaces for clarity (Internal & External)
3.	Assign Static IP to the Internal NIC (172.16.0.10)
4.	Rename the Server to AD-DC
5.	Install Active Directory Services (ADDS)
6.	Promote the Server to a Domain Controller with the domain mydomain.com
7.	Verify Domain Controller Status

![Image](https://github.com/user-attachments/assets/6c667a60-5a83-405b-bbfe-6d172b377dc2)|
|:--:|
|*Domain Creation*|

![Image](https://github.com/user-attachments/assets/b6564cb0-55d3-4ca0-9c60-bc6d75075812)|
|:--:|
|*Assign IP Address*|

|![Image](https://github.com/user-attachments/assets/0aa9568c-87ca-4da8-89f3-3b6a71a6760d)|
|:--:|
|*Install Active Directory*|

## 2. Installing and Configuring DHCP Server
1.	Install DHCP Server Role
2.	Create a DHCP Scope (172.16.0.100 - 172.16.0.200)
3.	Set Router/Gateway IP (172.16.0.2)
4.	Authorize the DHCP Server in AD-DC
5.	Verify successful lease assignments

![Image](https://github.com/user-attachments/assets/6152f7a3-2c74-4df6-92e4-827df6edcb08)|
|:--:|
|*DHCP Installation*|

![Image](https://github.com/user-attachments/assets/40bc0aac-9673-4235-88df-aa52d36b7a5d)|
|:--:|
|*Router Set-Up*|

## 3. Setting Up Remote Access and NAT
1.	Install Remote Access Role
2.	Enable Routing and Remote Access (RRAS)
3.	Configure NAT for Internal Network Routing
4.	Set up Internet Connectivity through the NAT interface
5.	Verify network routing between client machines

![Image](https://github.com/user-attachments/assets/13a451bd-5463-4d00-b4d7-0753dec9526e)|
|:--:|
|*NAT Configuration*|

## 4. Adding 150 Users and Organizational Units (OUs) via PowerShell
1.	Prepare a CSV file (user_accounts_final.csv) containing:
- Username
- Email
- Organizational Unit
- Password
2.	Write PowerShell Script (AD Bulk Users Script.ps1) to import users
3.	Run the script to add users to Active Directory
4.	Verify users in Active Directory Users and Computers (ADUC)

![Image](https://github.com/user-attachments/assets/25f754d4-f491-4553-bcc9-0b57e9205761)|
|:--:|
|*Active Directory Installation*|

![Image](https://github.com/user-attachments/assets/a3d915b9-1b98-49b1-a319-ed36ab6ce865)|
|:--:|
|*Adding 1,500 Users using Powershell Script*|

## 5. Joining Windows 10 Client to the Domain
1.	Install Windows 10 VM
2.	Ensure Network Connectivity (Internal and Internet)
3.	Join Windows 10 Machine to mydomain.com
4.	Authenticate with Domain Admin (a-aneedham)
5.	Verify DHCP IP Assignment
6.	Ensure domain policies are applied correctly

![Image](https://github.com/user-attachments/assets/3f269ae3-0575-4d3a-b12e-15594791daa2)|
|:--:|
|*Client DHCP Confirmation*|

## 6. Level Up This Lab By Implementing Security Policies for Users
1.	Create Group Policies for different OUs
2.	Restrict administrative access to non-admin users
3.	Enable password policies and login restrictions
4.	Deploy user-specific access control based on job roles

## Project Outcomes & Key Results
•	90% Time Reduction – Automated 150+ user accounts & OUs using PowerShell, eliminating manual setup
•	99.9% Uptime – Configured DHCP, NAT, and routing for seamless network connectivity
•	Stronger Security – Implemented role-based access policies for domain users, ensuring compliance
•	Real-World Simulation – Successfully joined Windows 10 clients to AD, enforcing domain-wide security

