# Active Directory Domain Services (AD DS)

## Overview

Active Directory Domain Services (AD DS) is a Microsoft directory service that provides centralized authentication, authorization, and management of users, computers, and other resources within a Windows domain.

It enables administrators to securely manage identities and control access to organizational resources.

---

## Key Components

### Domain

A domain is a logical group of users, computers, and devices that share a common directory database and security policies.

---

### Forest

A forest is the highest-level structure in Active Directory. It can contain one or more domains that share a common schema and global catalog.

---

### Organizational Unit (OU)

An Organizational Unit (OU) is a container used to organize users, groups, computers, and other OUs. It simplifies administration and allows Group Policies to be applied to specific objects.

---

### Domain Controller (DC)

A Domain Controller is a Windows Server that hosts Active Directory and authenticates users and computers within the domain.

---

## Common Active Directory Objects

- Users
- Groups
- Computers
- Organizational Units (OUs)
- Printers
- Shared Folders

---

## Authentication

Active Directory uses authentication protocols such as:

- Kerberos (default)
- NTLM (legacy)

These protocols verify user identities before granting access to network resources.

---

## Administrative Tasks

Windows Server administrators commonly perform:

- Create users and groups
- Reset user passwords
- Unlock user accounts
- Join computers to the domain
- Create Organizational Units
- Manage security groups
- Delegate administrative permissions
- Disable or delete inactive accounts

---

## Administration Tools

Common tools include:

- Active Directory Users and Computers (ADUC)
- Active Directory Administrative Center
- Server Manager
- PowerShell

---

## Benefits

- Centralized identity management
- Secure authentication
- Simplified administration
- Policy-based management
- Scalable enterprise infrastructure

---

## Best Practices

- Organize users and computers using OUs.
- Apply the principle of least privilege.
- Use security groups instead of assigning permissions directly to users.
- Regularly review inactive user accounts.
- Enable auditing for important administrative activities.
- Maintain regular backups of Domain Controllers.

---

## References

- Microsoft Learn
- Active Directory Documentation
