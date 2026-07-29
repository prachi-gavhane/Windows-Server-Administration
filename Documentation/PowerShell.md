# Windows Server PowerShell

## Overview

PowerShell is Microsoft's command-line shell and scripting language used to automate administrative tasks and manage Windows Server environments. It provides administrators with a powerful way to configure systems, manage Active Directory, monitor services, and automate repetitive tasks.

---

## Why Use PowerShell?

PowerShell helps administrators to:

- Automate repetitive tasks.
- Manage Windows Server roles and features.
- Administer Active Directory.
- Configure network settings.
- Monitor server health.
- Generate administrative reports.
- Manage services and processes.

---

## Common PowerShell Cmdlets

### Get Computer Information

```powershell
Get-ComputerInfo
```

---

### View Running Services

```powershell
Get-Service
```

---

### Restart a Service

```powershell
Restart-Service -Name Spooler
```

---

### View Running Processes

```powershell
Get-Process
```

---

### View Event Logs

```powershell
Get-EventLog -LogName System -Newest 20
```

---

### View IP Configuration

```powershell
Get-NetIPAddress
```

---

### Test Network Connectivity

```powershell
Test-Connection google.com
```

---

## Active Directory PowerShell

### View All Users

```powershell
Get-ADUser -Filter *
```

---

### View a Specific User

```powershell
Get-ADUser username
```

---

### Create a New User

```powershell
New-ADUser
```

---

### Reset a User Password

```powershell
Set-ADAccountPassword
```

---

### Unlock a User Account

```powershell
Unlock-ADAccount
```

---

## Common Administrative Tasks

Windows Server administrators commonly use PowerShell to:

- Manage Active Directory users and groups.
- Monitor Windows services.
- Restart services.
- Retrieve event logs.
- Configure network settings.
- Install Windows features.
- Automate repetitive administrative tasks.

---

## Best Practices

- Test scripts in a non-production environment before deployment.
- Use descriptive variable names.
- Follow the principle of least privilege.
- Document scripts with comments.
- Store scripts in a version control system such as GitHub.
- Keep PowerShell modules updated.

---

## References

- Microsoft Learn
- Windows PowerShell Documentation
- Active Directory PowerShell Module Documentation
