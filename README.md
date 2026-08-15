# fortigate-firewall-lab
FortiGate 300E configuration guides — password recovery, basic setup, and advanced security features (web filtering, IPS, VPN, DMZ)

**Prepared by:** [Venkat Kannan](https://github.com/venkatkannan-infra) — IT Infrastructure & Systems Administrator
**Device:** FortiGate 300E

Hands-on FortiGate configuration documentation, written from real lab and interview-preparation work. Covers device recovery, baseline network setup, and the full security profile stack — web filtering, DNS filtering, application control, IPS, IPsec VPN, and DMZ segmentation.

## Guides

| # | Guide | Covers |
|---|---|---|
| 1 | [Password Recovery](01-fortigate-password-recovery.md) | Maintainer-mode password reset via console cable |
| 2 | [Basic Configuration](02-fortigate-basic-configuration.md) | LAN/WAN interfaces, default route, outbound policy, SNAT |
| 3 | [Advanced Security Features](03-fortigate-advanced-security-features.md) | Web filtering, VIP/port forwarding, DNS filter, application control, IPS, remote-access IPsec VPN, DMZ |

## Environment

| Item | Detail |
|---|---|
| Device | FortiGate 300E |
| Management access | GUI + CLI (console) |
| Default management IP | `192.168.1.99` |
| Example topology | `port1` = LAN &nbsp;\|&nbsp; `wan1` / `port2` = WAN (ISP) &nbsp;\|&nbsp; `port3` = DMZ |

## Screenshots

All screenshots referenced in the guides are in [`/images`](images).

---

## Author

**Venkat Kannan**
IT Infrastructure & Systems Administrator — Active Directory, Microsoft 365, Azure, Fortinet, Windows Server, Networking (CCNA)
GitHub: [github.com/venkatkannan-infra](https://github.com/venkatkannan-infra)

*Part of my broader infrastructure and security engineering portfolio — see also the Wazuh SIEM lab and Azure Sentinel SIEM lab repositories.*

