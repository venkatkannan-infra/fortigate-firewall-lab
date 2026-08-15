# FortiGate Password Recovery (Maintainer Mode)

> **Device:** FortiGate 300E &nbsp;|&nbsp; **Guide 1 of 3** — FortiGate Configuration Series
> **Prepared by:** [Venkat Kannan](https://github.com/venkatkannan-infra)

Recovering admin access on a FortiGate appliance when the login password is lost or unknown. This procedure requires **physical/console access** to the device.

## Default Access

| Item | Value |
|---|---|
| Default Management IP | `192.168.1.99` |
| Default Username | `admin` |
| Default Password | *(blank / device-specific — see label)* |

## Recovery Procedure

If the password is incorrect, you can recover access using the console cable and **maintainer mode**:

1. Connect to the FortiGate using a **console cable** (RJ-45 to USB/serial).
2. Power-cycle (reset) the firewall.
3. Within **14 seconds** of the reboot, type `maintainer` at the FortiGate login prompt.
4. For the password, enter: `bcpb<SERIAL_NUMBER>` (**all caps**), where `<SERIAL_NUMBER>` is the unit's serial number.

> **Note:** The serial number can be found on the physical label on the chassis, or via `get system status` if you already have console access.

### Reset the Admin Password via CLI

Once logged in via maintainer mode, reset the `admin` account password:

```
config system admin
    edit admin
        set password YourNewPasswordHere
    end
```

### Confirm GUI Access

Once the password has been changed, navigate to the FortiGate GUI (`https://192.168.1.99`) and log in using the new password to confirm the reset was successful.

---

## Series Navigation

| Guide | Description |
|---|---|
| **1. Password Recovery** *(this guide)* | Maintainer-mode recovery via console cable |
| [2. Basic Configuration](02-fortigate-basic-configuration.md) | Interfaces, routing, and the primary outbound policy |
| [3. Advanced Security Features](03-fortigate-advanced-security-features.md) | Web/DNS filtering, application control, IPS, VPN, DMZ |

---

**Author:** Venkat Kannan — IT Infrastructure & Systems Administrator
**GitHub:** [github.com/venkatkannan-infra](https://github.com/venkatkannan-infra)

*This guide is part of a hands-on FortiGate 300E lab documentation series, published as part of an ongoing infrastructure and security engineering portfolio.*
