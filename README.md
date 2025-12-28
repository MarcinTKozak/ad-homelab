# ad-homelab

# Active Directory Home Lab

This repository documents my Active Directory home lab built for junior system administrator practice.
The project simulates a small enterprise Active Directory environment, including domain setup, organizational units, users, groups, and Group Policy configuration.

## Objectives
- Gain hands-on experience with Active Directory Domain Services
- Understand OU structure and role-based access control
- Practice user and group management
- Learn basic Group Policy configuration
- Document a real-world style lab project using Git and GitHub

## Technologies
- Windows Server 2019
- Active Directory Domain Services (AD DS)
- DNS
- Windows 11 Client
- VirtualBox

## Lab Structure
The lab is built using virtual machines and includes:
- 1 × Domain Controller (DC01)
- 1 × Windows Client (domain-joined)

## Project Structure

ad-homelab/
├── README.md
├── docs/
│ ├── task0-preparation.md
│ ├── task1-ad-installation.md
│ └── task2-users-ou-groups.md
└── scripts/
  └── README.md


## Progress
- [x] Task 0: Lab preparation and VM setup
- [x] Task 1: Active Directory installation and domain setup
- [x] Task 2: OU structure, users and security groups
- [x] Task 3: Group Policy configuration
  - Network drive mapping (GPO and logon script)
  - Desktop wallpaper policy
  - Domain password and account lockout policy
