# File Server

## Overview

A File Server is a Windows Server role that provides centralized storage for files and folders, allowing users to securely access and share data across a network.

It simplifies data management, improves collaboration, and enables administrators to control access using permissions.

---

## File Shares

A file share is a folder made available over the network for authorized users.

Example:

```
\\Server01\SharedFiles
```

Users can access shared folders based on the permissions assigned to them.

---

## Share Permissions

Share permissions control access to a shared folder over the network.

Common permission levels include:

- Read
- Change
- Full Control

---

## NTFS Permissions

NTFS permissions control access to files and folders stored on NTFS-formatted drives.

Common permissions include:

- Full Control
- Modify
- Read & Execute
- List Folder Contents
- Read
- Write

NTFS permissions provide more granular control than share permissions.

---

## Effective Permissions

When both Share and NTFS permissions are applied, the most restrictive permission determines the user's effective access.

Example:

- Share Permission: Full Control
- NTFS Permission: Read

Effective Permission:

```
Read
```

---

## Permission Inheritance

By default, files and folders inherit permissions from their parent folder.

Inheritance simplifies permission management and ensures consistent security settings.

---

## Access-Based Enumeration (ABE)

Access-Based Enumeration hides files and folders from users who do not have permission to view them.

This improves security and provides a cleaner user experience.

---

## Shadow Copies

Shadow Copies allow administrators and users to restore previous versions of files without recovering from backups.

Benefits include:

- Recover accidentally deleted files.
- Restore previous file versions.
- Reduce dependency on backup restoration.

---

## File Server Resource Manager (FSRM)

FSRM helps administrators manage storage by providing features such as:

- Storage quotas
- File screening
- Storage reports
- Classification management

---

## Common Administrative Tasks

Windows Server administrators commonly perform:

- Create shared folders.
- Configure NTFS permissions.
- Configure Share permissions.
- Enable Shadow Copies.
- Manage storage quotas.
- Monitor disk usage.
- Configure Access-Based Enumeration.

---

## Common Troubleshooting

### User Cannot Access Shared Folder

Possible causes:

- Incorrect Share permissions.
- Incorrect NTFS permissions.
- Network connectivity issues.
- User not in the required security group.

Resolution:

- Verify Share permissions.
- Verify NTFS permissions.
- Confirm group membership.
- Test network connectivity.

---

### Access Denied

Possible causes:

- Missing permissions.
- Inheritance disabled.
- Incorrect ownership.

Resolution:

- Review effective permissions.
- Restore inheritance if appropriate.
- Verify folder ownership.

---

## Best Practices

- Use Security Groups instead of assigning permissions directly to users.
- Apply the principle of least privilege.
- Keep Share permissions simple and manage access using NTFS permissions.
- Enable Shadow Copies for important file shares.
- Monitor storage usage regularly.
- Document shared folders and permission assignments.

---

## References

- Microsoft Learn
- Windows Server File Services Documentation
