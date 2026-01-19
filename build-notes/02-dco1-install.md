# DC01 – Windows Server 2022 Installation

## Objective
Deploy a Windows Server 2022 virtual machine to act as the Domain Controller for an isolated Active Directory lab.

## Environment
- Hypervisor: VMware Workstation Player
- Host OS: Windows 11 Pro
- Guest OS: Windows Server 2022 Standard (Desktop Experience)
- Disk: NVMe (Virtual)
- RAM: 4 GB
- CPU: 2 vCPUs
- Network: VMnet1 (Host-only)

## Installation Summary
- Booted from Windows Server 2022 ISO via EFI boot manager
- Performed a custom installation on unallocated disk space
- Verified successful disk creation (.vmdk)
- Completed initial administrator configuration
- Powered off VM to preserve clean baseline state

## Validation
- VM successfully boots to Windows Server login screen
- Virtual disk file confirmed present
