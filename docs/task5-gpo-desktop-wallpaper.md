# Task 5 – GPO Desktop Wallpaper

## Objective
Configure a domain-wide desktop wallpaper using Group Policy.

## Tasks completed

- Created folder: `C:\Wallpapers` on DC01
- Added wallpaper file: `company.jpg`
- Shared folder as: `\\DC01\Wallpapers`
- Share and NTFS permissions:
  - `Domain Users` – Read

- Created new GPO: `GPO_Wallpaper`
- Linked GPO to `Users` OU

- Configured policy:
  - User Configuration  
    → Policies  
    → Administrative Templates  
    → Desktop  
    → Desktop  
  - Policy: **Desktop Wallpaper**
  - State: Enabled
  - Path: `\\DC01\Wallpapers\company.jpg`
  - Style: Fill

## Result
Domain users receive a standardized desktop wallpaper after logon.
