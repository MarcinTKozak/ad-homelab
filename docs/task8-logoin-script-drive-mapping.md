# Task 8 – Active Directory Logon Script (Drive Mapping)

## Objective
Replace previous Z: drive GPO mapping with a logon script applied via Group Policy.

## Overview
This logon script automatically maps a network drive for users and logs actions for troubleshooting and auditing.

## Environment
- Windows Server (Domain Controller: DC01)
- Active Directory Domain: lab.local
- Windows client joined to the domain

## Network Share
- Server: DC01
- Share path: `\\DC01\Users$`
- Drive letter: Z:

## Script Functionality
- Removes any existing Z: drive mapping
- Maps network drive Z: to `\\DC01\Users$`
- Writes a log entry to a local log file for auditing
- Ensures mapping works on each user logon
