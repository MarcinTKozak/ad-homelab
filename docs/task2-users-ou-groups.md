# Task 2 – Organizational Units, Users and Groups

## Objective
Create a basic Active Directory structure with organizational units, users, and security groups.

## Tasks completed

### 1. Organizational Unit (OU) structure
Created the following OUs in the domain:

- IT
- HR
- Users
- Computers

> Note: Organizational Units are used for applying Group Policy Objects (GPOs) and managing administrative scope.

---

### 2. User creation
Created a standard domain user:

- First name: Jan  
- Last name: Kowalski  
- Username: `kowalskij`  

User account settings:
- Password set
- "User must change password at next logon" disabled (temporary for lab purposes)

---

### 3. Security groups
Created the following security group:

- Group name: `IT_Admins`
- Group scope: Global
- Group type: Security

Actions performed:
- Added user `kowalskij` to the `IT_Admins` group

---

## Result
The Active Directory environment now contains a basic organizational structure with users and role-based security groups.

## Notes
- OU structure will be expanded in future tasks
- Group membership will be used later for permissions and GPO filtering
