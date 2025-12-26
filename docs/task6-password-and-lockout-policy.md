# Task 6 – Domain Password and Account Lockout Policy

## Objective
Configure domain-wide password and account lockout policies using Default Domain Policy.

## Tasks completed

### Password Policy
Configured in **Default Domain Policy**:

- Enforce password history: 5
- Maximum password age: 90 days
- Minimum password age: 1 day
- Minimum password length: 10 characters
- Password must meet complexity requirements: Enabled
- Store passwords using reversible encryption: Disabled

### Account Lockout Policy
Configured in **Default Domain Policy**:

- Account lockout threshold: 5 invalid logon attempts
- Account lockout duration: 15 minutes
- Reset account lockout counter after: 15 minutes

### Policy update
- Ran `gpupdate /force` on DC01
- Ran `gpupdate /force` on CLIENT01

### Testing
- Verified password length enforcement (short password rejected)
- Verified account lockout after 5 failed logon attempts
- Confirmed account lockout status in Active Directory Users and Computers

## Result
Domain-wide password and lockout policies are enforced according to security best practices.
