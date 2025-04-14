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
|
