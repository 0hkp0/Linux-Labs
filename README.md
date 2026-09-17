# Linux Infrastructure & Network Administration Lab

A hands-on infrastructure lab built using VMware Workstation, OPNsense, and multiple Linux servers.

The goal is to practice real-world Linux system administration, networking, firewall configuration, troubleshooting, and infrastructure operations in a controlled environment.

## Current Lab

| Component           | Role              | Network       |
| ------------------- | ----------------- | ------------- |
| OPNsense            | Firewall / Router | WAN + LAN     |
| Rocky Linux 9.7     | Linux Server      | 10.20.20.0/24 |
| Oracle Linux 10 R2  | Linux Server      | 10.20.20.0/24 |
| Ubuntu Server 26.04 | Linux Server      | 10.20.20.0/24 |

### Network

```text
                    Internet
                        │
                 VMware VMnet8
                 10.10.10.0/24
                        │
                 ┌─────────────┐
                 │   OPNsense  │
                 │ WAN: DHCP   │
                 │ LAN: .1     │
                 └──────┬──────┘
                        │
                 VMware VMnet10
                 10.20.20.0/24
                        │
          ┌─────────────┼─────────────┐
          │             │             │
       Rocky         Oracle        Ubuntu
      .144/24        .187/24       .152/24
```

## Completed

* Installed and configured OPNsense
* Created separate WAN and LAN networks using VMware
* Configured OPNsense LAN as `10.20.20.1/24`
* Connected Rocky Linux, Oracle Linux and Ubuntu Server to the LAN
* Verified communication between Linux servers
* Verified connectivity from Linux servers to OPNsense
* Verified Internet connectivity through OPNsense
* Troubleshot and corrected an OPNsense WAN/LAN interface mapping issue
* Verified the final network configuration

## Current Status

**Phase 1 — Network Foundation: Complete ✅**

**Phase 2 — Linux Server Connectivity: Complete ✅**

Further server administration and infrastructure scenarios will be added progressively.
