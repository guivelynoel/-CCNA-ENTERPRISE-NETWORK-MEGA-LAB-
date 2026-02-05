# Troubleshooting & Packet Tracer Limitations

## 📌 Purpose of This Document
This document summarizes the **errors encountered**, **troubleshooting steps**, and **limitations of Cisco Packet Tracer** during the implementation of the **CCNA Enterprise Network Mega Lab**.

Rather than hiding issues, this section demonstrates:
- Real-world troubleshooting methodology
- Understanding of IOS behavior
- Awareness of simulation tool limitations
- Professional engineering judgment

---

## 1️⃣ EtherChannel (Port-Channel) Issues

### ❌ Problem Encountered
- Port-channel links showing **red / suspended**
- Error messages such as: EC-5-CANNOT_BUNDLE2: VLAN mask is different

  ### 🔍 Root Cause
- Member interfaces had **different trunk configurations**
- VLAN allowed lists were not identical
- Native VLAN mismatches between links
- Interfaces still assigned to VLAN 1 before full trunk configuration

### ✅ Resolution
- Ensured **identical configuration** on all member interfaces:
- Trunk mode
- Allowed VLAN list
- Native VLAN
- Removed interfaces from access mode before adding to channel-group
- Verified with:show etherchannel summary
                show interfaces trunk

  ### 🧠 Lesson Learned
EtherChannel requires **bit-for-bit identical configurations** across all bundled interfaces.

---

## 2️⃣ IP SLA & Tracking Not Supported as Expected

### ❌ Problem Encountered
Commands rejected:ip sla 1
icmp-echo 8.8.8.8
track 1 interface g0/1 line-protocol

### 🔍 Root Cause
- Cisco Packet Tracer **does not fully support IP SLA**
- Some IOS features are **disabled or partially implemented**
- `track` objects tied to SLA are unreliable in PT

### ✅ Decision Taken
- **Step skipped intentionally**
- Redundancy concept documented conceptually
- Focus kept on supported CCNA objectives

### 🧠 Lesson Learned
Packet Tracer is a **learning simulator**, not a full IOS emulator.

---

## 3️⃣ QoS (Quality of Service) Limitations

### ❌ Problem Encountered
Unsupported commands:
class-map match-any VOICE
match dscp ef
mls qos vlan-based
mls qos trust cos

### 🔍 Root Cause
- Packet Tracer **does not support advanced QoS**
- Catalyst 3560 PT image has **QoS features disabled**
- DSCP, CoS, and MQC are not implemented

### ✅ Decision Taken
- QoS configuration **not enforced**
- QoS concepts documented theoretically
- Voice VLAN still implemented logically

### 🧠 Lesson Learned
Understanding *why* something cannot be configured is as important as knowing *how*.

---

## 4️⃣ NAT & Internet Cloud Behavior

### ❌ Problem Encountered
- Internet PC unable to reach public IPs
- HTTP tests failing despite correct NAT config
- Cloud device behaving inconsistently

### 🔍 Root Cause
- Packet Tracer **Cloud device is highly simplified**
- No true ISP routing table
- NAT behavior is simulated, not real
- No real upstream Internet

### ✅ Decision Taken
- NAT validated using:
  - Internal-to-DMZ reachability
  - Router-level tests (ping / telnet)
- Internet simulation considered **conceptual only**

### 🧠 Lesson Learned
Packet Tracer is **not suitable for realistic Internet emulation**.

---

## 5️⃣ DNS Resolution Issues

### ❌ Problem Encountered
- Hostnames not resolving from client PCs
- DNS queries failing despite server configuration

### 🔍 Root Cause
- DNS service in PT is **basic**
- NAT + DNS combinations unreliable
- Cloud does not forward DNS queries correctly

### ✅ Resolution
- Used **IP-based testing**
- Verified services locally inside VLANs
- DNS considered **demonstration-only**

---

## 6️⃣ Interface Naming & Platform Differences

### ❌ Problem Encountered
- Confusion between `G0/1` vs `Gig0/1`
- Some commands rejected due to interface mismatch

### 🔍 Root Cause
- Packet Tracer device models differ from real hardware
- Interface naming depends on **specific PT image**

### ✅ Resolution
- Verified interface names using: show ip interface brief

- ---

## 7️⃣ Why These Limitations Are Acceptable

### ✅ Key Takeaway
In real enterprise environments:
- Engineers adapt to platform constraints
- Designs are validated across tools
- Documentation explains decisions

This lab demonstrates:
- Correct **engineering logic**
- Correct **troubleshooting mindset**
- Awareness of **simulation vs production**

---

## 🏁 Final Conclusion
All skipped or adjusted steps were:
- **Intentional**
- **Justified**
- **Documented**

This reflects **real-world network engineering practices**, not just exam memorization.

