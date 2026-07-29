# Dynamic Host Configuration Protocol (DHCP)

## Overview

Dynamic Host Configuration Protocol (DHCP) is a network service that automatically assigns IP addresses and other network configuration settings to devices connected to a network. It eliminates the need to manually configure IP addresses for each device.

DHCP simplifies network administration and helps prevent IP address conflicts.

---

## How DHCP Works

When a device connects to the network, DHCP follows the DORA process:

1. **Discover** – The client broadcasts a request for an IP address.
2. **Offer** – The DHCP server offers an available IP address.
3. **Request** – The client requests the offered IP address.
4. **Acknowledge** – The server confirms the assignment.

---

## DHCP Components

### Scope

A scope is a range of IP addresses that the DHCP server can assign to clients.

Example:

```
192.168.1.100 – 192.168.1.200
```

---

### Lease

A lease is the period during which a client can use an assigned IP address before it must renew it.

---

### Reservation

A reservation assigns a specific IP address to a device based on its MAC address.

This ensures the device always receives the same IP address.

---

### Exclusion Range

An exclusion range prevents specific IP addresses within a scope from being assigned automatically.

---

## Information Assigned by DHCP

Along with an IP address, DHCP can assign:

- Subnet Mask
- Default Gateway
- DNS Server
- Domain Name
- Lease Duration

---

## Common Administrative Tasks

Windows Server administrators commonly perform:

- Create and configure DHCP scopes.
- Configure exclusion ranges.
- Create IP reservations.
- Monitor active leases.
- Authorize DHCP servers in Active Directory.
- Backup and restore DHCP configurations.

---

## DHCP Management Tools

- DHCP Manager
- Server Manager
- Windows Admin Center
- PowerShell

---

## Common Troubleshooting

### Client Not Receiving an IP Address

Possible causes:

- DHCP Server is offline.
- Scope has no available addresses.
- Network connectivity issues.
- DHCP service is stopped.

Resolution:

- Verify the DHCP service is running.
- Check available IP addresses in the scope.
- Renew the client's IP address:

```cmd
ipconfig /release
ipconfig /renew
```

- Verify network connectivity.

---

### IP Address Conflict

Possible causes:

- Duplicate static IP address.
- Incorrect reservation.
- Misconfigured DHCP scope.

Resolution:

- Identify duplicate addresses.
- Review reservations.
- Correct the scope configuration.

---

## Best Practices

- Regularly back up DHCP configurations.
- Configure DHCP failover where possible.
- Monitor scope utilization.
- Use reservations for critical devices.
- Maintain accurate DHCP documentation.

---

## References

- Microsoft Learn
- Windows Server DHCP Documentation
