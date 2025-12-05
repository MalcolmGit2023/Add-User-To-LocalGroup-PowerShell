# Add User to Local Group PowerShell Script

## Overview
This PowerShell script adds a specified user to any local group on Windows. It supports both on-prem Active Directory and Azure AD accounts.

## Example Usage
```powershell
Add-LocalGroupMember -Group "Administrators" -Member "azuread\user@domain.com"
```

## When to Use
- Grant local group permissions to users for roles like:
  - Administrators
  - Remote Desktop Users
  - Hyper-V Administrators
  - Any custom local group
- Useful for IT admins managing on-prem or cloud domain accounts.

## Requirements
- Administrator privileges.
- PowerShell 5.1 or later.
- LocalGroupMember cmdlet available.
- Correct domain prefix:
  - `domain\username` for on-prem AD.
  - `azuread\email` for Azure AD accounts.

## Notes
- Always verify the group name exists before running.
- Adding users to privileged groups can impact security—use with caution.

---

### Disclaimer
Use at your own risk. Ensure you have proper permissions and understand the impact of adding users to local groups.
