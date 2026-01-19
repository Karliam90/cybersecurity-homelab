# Domain Controller Setup (Windows Server 2022)

## Purpose
Deploy a Windows Server 2022 Domain Controller to provide centralized authentication, DNS, and directory services for the home lab environment. This server serves as the core identity and management system for all domain-joined resources.

---

## Environment Details

- **Hostname:** DC01
- **Operating System:** Windows Server 2022 (Desktop Experience)
- **Virtualization Platform:** VMware Workstation Player
- **CPU:** 2 vCPUs
- **Memory:** 4 GB RAM
- **Disk:** 60 GB (single file)
- **Network Type:** Host-only (VMnet1)

---

## Network Configuration

- **IP Address:** 192.168.100.10 (Static)
- **Subnet Mask:** 255.255.255.0
- **Default Gateway:** Not configured (isolated network)
- **DNS Server:** 192.168.100.10 (self)

> A static IP was configured prior to promoting the server to a Domain Controller to ensure consistent DNS and authentication services.

---

## Domain Information

- **Domain Name:** lab.local
- **Forest Functional Level:** Windows Server 2016
- **Domain Functional Level:** Windows Server 2016

---

## Installation & Configuration Steps

1. Installed Windows Server 2022 using Desktop Experience
2. Renamed the server to `DC01`
3. Assigned a static IP address
4. Installed the **Active Directory Domain Services (AD DS)** role
5. Promoted the server to a Domain Controller
6. Installed DNS during promotion
7. Rebooted and verified domain services

---

## Validation & Testing

- Successfully logged in using domain administrator credentials
- Verified Active Directory services were running
- Confirmed DNS functionality via name resolution
- Verified server role using Server Manager

---

## Issues Encountered & Resolutions

### Issue: Network Adapter Initially Set to NAT
- **Impact:** Risk of improper DNS behavior during domain promotion
- **Resolution:** Reconfigured network adapter to Host-only (VMnet1) before promoting to Domain Controller

### Issue: VMware Did Not Prompt for Network During VM Creation
- **Resolution:** Network adapter was manually configured in VM settings prior to powering on the VM

---

## Security Considerations

- Server is isolated from the internet using a host-only network
- Administrative access limited to domain credentials
- Snapshots taken prior to major configuration changes

---

## Current Status
✅ Domain Controller deployed and operational

---

## Next Steps
- Create Organizational Units (OUs)
- Add domain users and groups
- Configure Group Policy Objects (GPOs)
- Join Windows client to the domain
