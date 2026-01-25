# Base Device Configuration (Step 3)

## Purpose
This document defines the standard base configuration applied to all routers
and switches in the CCNA Enterprise Mega Lab.

The goal is to:
- Establish secure management access
- Prevent common CLI usability issues
- Standardize device behavior
- Prepare devices for SSH, logging, and monitoring

This configuration is applied **before** VLANs, routing, or services.

---

## 1. Hostname Configuration


hostname <DEVICE-NAME>
What it does:
Sets a unique name for the device.

Why it matters:

-Identifies the device in logs and monitoring

-Prevents confusion in multi-device environments

---

## 2. Disable DNS Lookup 
no ip domain-lookup
What it does:

Stops the device from trying to resolve mistyped commands as DNS names.

Why it matters:

--Prevents CLI freezing
==Improves operator efficiency

## 3. Secure Privileged EXEC Mode

enable secret yourpassword

What it does:
Sets an encrypted password for privileged mode.

Why it matters:

---Protects administrative access
---Required security baseline in enterprise networks

## 4. Local Administrator Account
username admin privilege 15 secret Admin@123

What it does:
Creates a local admin user with full privileges.

Why it matters:

--Required for SSH authentication
--Enables user-level accountability

## 5. Console Line Security
line console 0
 password Console@123
 login
 logging synchronous
 exit

What it does:
Secures physical console access and improves CLI usability.

Why it matters:

---Prevents unauthorized console access
---Keeps command output readable during log events

## 6. VTY Line Configuration (SSH Preparation)
line vty 0 4
 login local
 transport input ssh
 exit


What it does:
Prepares virtual terminal lines for SSH access.

Why it matters:

---Disables insecure Telnet
---Enables secure remote management

### 7. Password Encryption
service password-encryption

What it does:
Encrypts plaintext passwords in the running configuration.
Why it matters:

---Prevents password exposure
---Basic security requirement

### 8. Legal Warning Banner
banner motd ^
UNAUTHORIZED ACCESS IS PROHIBITED.
ALL ACTIVITY IS MONITORED.
^

What it does:
Displays a legal warning before login.

Why it matters:

---Required in many enterprise environments
---Provides legal notice of monitoring

### 9. Save Configuration
write memory

What it does:
Saves the running configuration to startup configuration.

Why it matters:

Ensures changes persist after reboot

Verification Commands
show running-config | section username
show running-config | section line
show running-config | include hostname


These commands confirm the base configuration is applied correctly.


