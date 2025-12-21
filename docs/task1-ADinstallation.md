# Task 1 – Active Directory Installation and Domain Setup

## Objective
Install and configure Active Directory Domain Services for the home lab environment.

## Environment
- Server OS: Windows Server 2019
- Server Name: DC01
- Domain Name: lab.local

## Tasks completed

### 1. Server preparation
- Verified static IP configuration
- Verified server hostname (DC01)

### 2. Active Directory Domain Services installation
- Installed **Active Directory Domain Services** role
- Installed **DNS Server** role
- Completed post-installation configuration

### 3. Domain configuration
- Created a new forest
- Domain name: lab.local
- Set domain and forest functional level
- Configured Directory Services Restore Mode (DSRM) password

## Result
The domain controller was successfully installed and the Active Directory domain is operational.

## Notes
- This server will act as the primary domain controller for the lab
- Additional services and policies will be configured in subsequent tasks
