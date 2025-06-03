This is the **fully detailed Week 4 Instructor Script** for the **PCI-Aware System Design Training Course**, focusing on **Logging & Monitoring**.

---

# 🎙️ **Week 4 – Instructor Script**

### Theme: Logging, Monitoring & PCI DSS Audit Trails

📌 **PCI DSS Focus**: Requirements **10.2–10.7**, **10.4.1.1**, **12.10.5**

---

## 🕘 **Session Duration**: 90 minutes (adjustable)

| Segment                            | Duration | Purpose                                                 |
| ---------------------------------- | -------- | ------------------------------------------------------- |
| Welcome Back + Log Story           | 10 mins  | Set the scene with a breach story involving bad logging |
| Intro to Logging Concepts          | 15 mins  | Discuss logs as detective tools                         |
| PCI DSS Log Requirements Deep Dive | 15 mins  | Map Req 10.x and 12.10.5 to system design               |
| Hands-On: Log Field Mapping        | 20 mins  | Use `logging-map-pci10.json` to identify log insights   |
| Policy Review & Tamper Protections | 15 mins  | Walkthrough `log-retention-standards.md`                |
| Reflection + Wrap-Up               | 15 mins  | Discussion + prepare students for access control topics |

---

## 🎤 **1. Welcome + Real-World Log Story (10 mins)**

🎤 Say:

> “Welcome back! We’ve encrypted our data—now let’s make sure we can tell when someone tries to mess with it.”

🧠 Share this short story:

> “In a real PCI incident, attackers accessed an S3 bucket—but logs weren’t enabled. The breach went undetected for **three months**, because there were **no records** of access. It was only discovered when cardholders started complaining.”

📢 Ask:

> “What’s worse than getting breached? Getting breached and not knowing.”

---

## 📊 **2. Logging Concepts 101 (15 mins)**

Define:

* **Log event**: A recorded action or state
* **Audit trail**: Sequence of events that prove what happened
* **Log lifecycle**: Generate → Store → Monitor → Retain → Archive

Discuss:

* Types of logs: **Authentication**, **Access**, **Change**, **System**
* Format and integrity: timestamps, hashes, log aggregation

🧠 Analogy:

> “Logs are the flight recorder of your system—don’t fly without one.”

📢 Ask:

> “What’s your current setup for log collection—any central aggregation in place?”

---

## 📎 **3. PCI DSS Requirements Mapping (15 mins)**

Use this mapping to guide discussion:

| PCI Requirement   | Purpose                                              | Design Impact                                         |
| ----------------- | ---------------------------------------------------- | ----------------------------------------------------- |
| **10.2.1–10.2.7** | Record user activity (logins, access, privilege use) | Ensure application and system logs capture key fields |
| **10.3.1**        | Include user ID, timestamp, result, system component | Structured log formats (e.g., JSON fields)            |
| **10.4.1.1**      | Use synchronized, accurate time                      | Use NTP or cloud time sync                            |
| **10.5.1**        | Protect logs from unauthorized modification          | Use WORM, permissions, encryption                     |
| **10.7.1**        | Retain logs for at least 12 months                   | Set log retention policies                            |
| **12.10.5**       | Trigger IR process on suspicious logs                | Tie alerts to incident playbooks                      |

🎤 Say:

> “A great system won’t help if your logs can’t prove what happened—or if they’re deleted.”

---

## 🔍 **4. Hands-On Log Field Mapping (20 mins)**

Open: `📁Addendum: logging-map-pci10.json`

### Instructions:

1. Show example:

```json
"timestamp": "10.4.1.1",
"user_id": "10.2.1",
"event_type": "10.2.2"
```

2. Ask teams or individuals to pick **3 fields** from the file and:

   * Explain what it tells an assessor
   * Identify where that log might originate (app, infra, DB, etc.)
   * Link it to an attack or incident use case

🧠 Example:

> **event\_type (10.2.2)**: Helps detect unauthorized changes
> **source\_ip (10.2.4)**: Useful for geo-blocking or correlation
> **log\_integrity (10.5.1)**: Critical for legal defensibility

📢 Group Share:

> “Which field felt the most critical to proving suspicious behavior?”

---

## 📜 **5. Policy & Log Protections (15 mins)**

Open: `📁Addendum: log-retention-standards.md`

### Review Highlights:

* Retention Periods:

  * Security logs → 12 months
  * Application logs → 90 days
* Protections:

  * Write-once (WORM) storage
  * Hashing or checksums
  * Access control + separation of duties

🎤 Ask:

> “How many of you have had to **pull logs for a PCI audit**? What was the biggest challenge?”

Highlight:

* Storage ≠ Security → Retention ≠ Integrity
* Centralization is key (e.g., ELK, Splunk, Fluentd, CloudWatch)

---

## ✏️ **6. Reflection + Wrap-Up (15 mins)**

📘 Reflect Prompt from Workbook:

> “Why is it important to prevent tampering with logs?”

Let students write or share their responses. Then summarize:

🎓 **Key Takeaways**:

* PCI DSS cares deeply about logs because **they prove intent and history**.
* Logging ≠ monitoring. You must also analyze and alert.
* Accurate time and immutability = credible evidence.

---

## 📦 Deliverables Recap

| Resource                     | Description                          |
| ---------------------------- | ------------------------------------ |
| `logging-map-pci10.json`     | PCI log field mappings               |
| `log-retention-standards.md` | Example policy for Req 10.3.1–10.7.1 |
| Student Workbook – Week 4    | Objectives, reflection prompt        |

---

## 📢 Preview Week 5:

> “Next week, we build gates and play defenders—we’re going into **Access Control** and **Incident Response**. Get ready for a live role simulation.”

---
