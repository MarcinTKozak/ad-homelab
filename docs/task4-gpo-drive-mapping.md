# Task 4 – Group Policy Drive Mapping (Network Drive Z:)

## Objective
Configure a network drive mapping for domain users using Group Policy Preferences.

## Environment
- Domain Controller: DC01
- Domain Name: lab.local
- Target OU: Users
- Network Drive: Z:

---

## Tasks completed

### 1. File share creation on DC01
Created a shared folder to store user data.

Steps:
- Created folder: `C:\Shares\Users`
- Enabled advanced sharing
- Share name: `Users$` (hidden share)

Share permissions:
- Removed default permissions
- Added `Domain Users` with Full Control

NTFS permissions:
- `Domain Users`: Modify

---

### 2. Group Policy Object creation
Created a new Group Policy Object for drive mapping.

Steps:
- Opened Group Policy Management
- Created and linked a new GPO to the `Users` OU

GPO name:
- `GPO_Map_Drive_Z`

---

### 3. Drive mapping configuration
Configured drive mapping using Group Policy Preferences.

Path:
- User Configuration  
  → Preferences  
  → Windows Settings  
  → Drive Maps  

Settings:
- Action: Create
- Location: `\\DC01\Users$`
- Drive Letter: `Z:`
- Label as: `User Share`

---

## Result
Domain users automatically receive a mapped network drive (Z:) upon login.

## Notes
- Group Policy Preferences allow flexible drive mapping without login scripts
- Hidden shares (`$`) prevent users from browsing shares manually
