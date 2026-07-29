# Group Policy (GPO)

## Overview

Group Policy is a Windows feature that allows administrators to centrally manage and configure operating system settings, user environments, security policies, and applications for computers and users in an Active Directory domain.

Using Group Policy helps ensure consistency, security, and compliance across an organization's IT infrastructure.

---

## Group Policy Objects (GPOs)

A Group Policy Object (GPO) is a collection of settings that can be applied to users or computers.

A GPO can configure:

- Password policies
- Desktop settings
- Software installation
- Security settings
- Windows Updates
- Login and logout scripts
- Folder redirection

---

## Types of Group Policy

### Local Group Policy

Applies only to the local computer.

Used in standalone systems that are not joined to a domain.

---

### Domain Group Policy

Stored in Active Directory and applied to users and computers throughout the domain.

Managed using the **Group Policy Management Console (GPMC)**.

---

## Group Policy Processing Order

Group Policies are applied in the following order, commonly referred to as **LSDOU**:

1. Local
2. Site
3. Domain
4. Organizational Unit (OU)

Policies applied later override earlier settings when conflicts occur.

---

## Common Administrative Tasks

Windows Server administrators commonly perform:

- Create new GPOs.
- Link GPOs to Organizational Units (OUs).
- Configure password and account lockout policies.
- Deploy security settings.
- Configure Windows Update policies.
- Restrict Control Panel or Command Prompt access.
- Configure login and startup scripts.
- Force Group Policy updates.

---

## Group Policy Management Tools

- Group Policy Management Console (GPMC)
- Local Group Policy Editor (gpedit.msc)
- Server Manager
- PowerShell

---

## Common Troubleshooting

### Group Policy Not Applying

Possible causes:

- Incorrect OU placement.
- Security filtering.
- WMI filtering.
- Replication delays.
- Client not updated.

Resolution:

- Run:

```cmd
gpupdate /force
```

- Verify applied policies:

```cmd
gpresult /r
```

- Check Event Viewer for Group Policy errors.
- Confirm the user or computer is in the correct OU.

---

## Benefits

- Centralized administration
- Consistent security settings
- Simplified user management
- Automated policy deployment
- Reduced administrative effort

---

## Best Practices

- Use descriptive names for GPOs.
- Link GPOs only where required.
- Test new GPOs before deploying to production.
- Avoid unnecessary policy inheritance blocking.
- Document all Group Policy changes.
- Review unused GPOs periodically.

---

## References

- Microsoft Learn
- Windows Server Group Policy Documentation
