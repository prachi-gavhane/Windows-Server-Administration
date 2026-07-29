# Microsoft Entra Connect

## Overview

Microsoft Entra Connect (formerly Azure AD Connect) is a synchronization tool that connects an on-premises Active Directory environment with Microsoft Entra ID (formerly Azure Active Directory). It enables organizations to maintain a hybrid identity by synchronizing users, groups, and other directory objects.

---

## Benefits

Microsoft Entra Connect provides:

- Hybrid identity
- Single Sign-On (SSO)
- Centralized identity management
- Synchronization of users and groups
- Improved user experience
- Simplified administration

---

## Authentication Methods

### Password Hash Synchronization (PHS)

Synchronizes password hashes from on-premises Active Directory to Microsoft Entra ID.

Benefits:

- Simple deployment
- High availability
- No additional infrastructure required

---

### Pass-through Authentication (PTA)

Validates user passwords directly against the on-premises Active Directory during sign-in.

Benefits:

- Passwords remain on-premises
- Supports hybrid authentication

---

### Federation

Uses Active Directory Federation Services (AD FS) to authenticate users.

Typically used by organizations with advanced authentication requirements.

---

## Synchronization

Microsoft Entra Connect synchronizes:

- Users
- Groups
- Contacts
- Password hashes (if PHS is enabled)

Synchronization runs automatically based on the configured schedule.

---

## Common Administrative Tasks

Windows Server administrators commonly perform:

- Install Microsoft Entra Connect.
- Configure directory synchronization.
- Select synchronization options.
- Configure Password Hash Synchronization.
- Configure Pass-through Authentication.
- Monitor synchronization health.
- Resolve synchronization errors.

---

## Common Troubleshooting

### User Not Syncing

Possible causes:

- User is outside the selected Organizational Unit (OU).
- Synchronization has not completed.
- Synchronization errors.

Resolution:

- Verify OU filtering.
- Force a synchronization cycle.
- Review synchronization logs.
- Confirm the user exists in Active Directory.

---

### Password Changes Not Syncing

Possible causes:

- Password Hash Synchronization disabled.
- Synchronization service issues.

Resolution:

- Verify Password Hash Synchronization is enabled.
- Check synchronization status.
- Run a manual synchronization if required.

---

## Best Practices

- Monitor synchronization health regularly.
- Keep Microsoft Entra Connect updated.
- Synchronize only required Organizational Units.
- Document synchronization configuration.
- Review synchronization errors promptly.

---

## References

- Microsoft Learn
- Microsoft Entra Connect Documentation
