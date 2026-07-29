# Domain Name System (DNS)

## Overview

The Domain Name System (DNS) is a network service that translates human-readable domain names into IP addresses. It enables users and applications to locate servers and services on a network without remembering numerical IP addresses.

DNS is a critical component of Active Directory because domain controllers rely on it for locating and authenticating resources.

---

## How DNS Works

When a user enters a domain name (for example, `www.example.com`), the DNS server:

1. Receives the query.
2. Searches its DNS records.
3. Returns the corresponding IP address.
4. The client connects to the destination server.

---

## Common DNS Records

### A Record

Maps a hostname to an IPv4 address.

Example:

```
server01 → 192.168.1.10
```

---

### AAAA Record

Maps a hostname to an IPv6 address.

---

### CNAME Record

Creates an alias for another hostname.

Example:

```
mail.company.com
        ↓
server01.company.com
```

---

### MX Record

Specifies the mail server responsible for receiving emails for a domain.

---

### PTR Record

Maps an IP address back to a hostname (Reverse Lookup).

---

### NS Record

Identifies the authoritative DNS servers for a domain.

---

## DNS Zones

Common DNS zone types include:

- Forward Lookup Zone
- Reverse Lookup Zone
- Primary Zone
- Secondary Zone
- Stub Zone

---

## Common Administrative Tasks

Windows Server administrators commonly perform:

- Create DNS zones.
- Add or modify DNS records.
- Configure Forward and Reverse Lookup Zones.
- Verify DNS name resolution.
- Troubleshoot DNS issues.
- Monitor DNS server health.

---

## DNS Management Tools

- DNS Manager
- Server Manager
- Windows Admin Center
- PowerShell
- Command Prompt (`nslookup`, `ipconfig`)

---

## Common Troubleshooting

### Name Resolution Failure

Possible causes:

- Incorrect DNS server
- Missing DNS record
- Network connectivity issues

Resolution:

- Verify DNS server settings.
- Check DNS records.
- Flush the DNS cache:

```cmd
ipconfig /flushdns
```

- Test name resolution:

```cmd
nslookup hostname
```

---

## Best Practices

- Configure redundant DNS servers.
- Regularly back up DNS zones.
- Remove stale DNS records.
- Secure DNS servers with appropriate permissions.
- Monitor DNS replication and health.

---

## References

- Microsoft Learn
- Windows Server DNS Documentation
