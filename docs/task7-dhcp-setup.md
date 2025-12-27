# Task 7 – DHCP Server Setup and Integration with AD

## Objective
Configure a domain-integrated DHCP server to assign IP addresses centrally and update DNS automatically.

## Tasks completed

- Installed DHCP Server role on DC01
  - GUI: Server Manager
  - PowerShell: `Install-WindowsFeature DHCP -IncludeManagementTools`

- Authorized DHCP in Active Directory
  - GUI: DHCP Server authorization using Domain Admin
  - PowerShell: `Add-DhcpServerInDC -DnsName DHCP01.lab.local -IPAddress 192.168.56.10`

- Created DHCP scope
  - Network: 192.168.56.0/24
  - Range: 192.168.56.100 – 192.168.56.200
  - Exclusions: 192.168.56.1 – 192.168.56.20
  - Lease duration: 8 days
  - PowerShell: `Add-DhcpServerv4Scope -Name "LAN-SCOPE" -StartRange 192.168.56.100 -EndRange 192.168.56.200 -SubnetMask 255.255.255.0 -State Active`

- Configured DHCP options
  - Option 003 – Default Gateway: 192.168.56.1
  - Option 006 – DNS Server: 192.168.56.10

- Enabled DNS integration
  - Dynamic updates: Enabled
  - Discard records when lease deleted: Enabled

- Tested client configuration
  - `ipconfig /release` / `ipconfig /renew`
  - Received IP in scope, correct DNS and gateway
  - DNS records created automatically
