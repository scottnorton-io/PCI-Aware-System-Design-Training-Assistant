This is the **fully detailed Week 5 Instructor Script** for the **PCI-Aware System Design Training Course**, focused on **Access Control & Incident Response**.

---

# 🎙️ **Week 5 – Instructor Script**

### Theme: Role-Based Access & Incident Response Simulation

📌 **PCI DSS Focus**: Requirements **7.2.2**, **8.3.1**, **12.10.5**

---

## 🕘 **Session Duration**: 90 minutes (adjustable)

| Segment                               | Duration | Purpose                                              |
| ------------------------------------- | -------- | ---------------------------------------------------- |
| Welcome Back & Role-Setting           | 10 mins  | Introduce theme, recap log importance                |
| Access Control Concepts & PCI Mapping | 20 mins  | Review roles, privileges, MFA, and link to Req 7 & 8 |
| Walkthrough: Access Control Template  | 15 mins  | Use policy sample to map user roles                  |
| Incident Simulation Setup             | 10 mins  | Assign roles and introduce simulated breach          |
| Run the Response Simulation           | 20 mins  | Playbook-driven incident response                    |
| Debrief, Reflection & Wrap-Up         | 15 mins  | Discuss lessons, tie to PCI, prep for capstone       |

---

## 🎤 **1. Welcome Back + Role-Setting (10 mins)**

🎤 Say:

> “Welcome to Week 5! Now we move from prevention to **detection and action**. We’re stepping into the roles of real operators.”

🧠 Warm-up:

* Ask: “What roles in your org can log in to production systems?”
* Ask: “When was the last time you reviewed who has admin access?”

📎 Recap:

> Last week’s logs tell you **what happened**. This week is about **who had access** and **how you responded.**

---

## 🔐 **2. Access Control Concepts & PCI DSS (20 mins)**

Explain:

### 🧠 Role-Based Access Control (RBAC)

* Only give access **based on business need**
* Enforce **least privilege**
* Keep access **auditable**

### 🔐 MFA (Multi-Factor Authentication)

* Required for **all remote access**
* Must protect **admin logins** and **interactive access**

### 🚪 PCI DSS Requirements:

| PCI Req   | Purpose                                      | Application                                 |
| --------- | -------------------------------------------- | ------------------------------------------- |
| **7.2.2** | Assign roles based on business justification | IAM policies, access provisioning workflows |
| **8.3.1** | Require MFA for all admin/remote access      | VPNs, consoles, SSH                         |
| **8.6.1** | No shared admin credentials                  | Unique accounts, no shared root passwords   |

📢 Ask:

> “What happens when a single admin account is used by 3 people? Can you truly audit who did what?”

---

## 📑 **3. Walkthrough: Access Control Template (15 mins)**

Open: `📁Addendum: access-control-policy-template.md`

### Walk through sections:

* **Roles**:

  * Admin, Developer, Read-only Auditor
* **Controls**:

  * MFA required
  * Unique IDs only
  * Quarterly access reviews

📢 Discussion:

> “What’s missing in this template for your environment? Do you enforce automatic access revocation?”

🧠 Emphasize:

> Policies don’t mean anything without **implementation + review**.

---

## 🚨 **4. Incident Simulation Setup (10 mins)**

### Scenario:

> “You receive a PagerDuty alert: anomalous SSH login to a production DB from an unknown IP at 2:47 AM.”

### Assign roles:

* Security Analyst
* Incident Commander
* Developer (on-call)
* Compliance Officer
* External Assessor (observer)

Distribute or display: `📁Addendum: incident-playbook-v1.md`

---

## 🧪 **5. Run the Simulation (20 mins)**

Follow the 4 phases from the playbook:

### Phase 1 – Detection

* Slack alert triggers escalation
* Analyst investigates IP and logs

### Phase 2 – Containment

* Isolate the DB node
* Rotate secrets or access keys

### Phase 3 – Notification

* Open incident ticket
* Inform compliance officer

### Phase 4 – Recovery

* Roll back to backup
* Archive logs and tag the timeline

📢 Prompt during action:

> “Where do you see PCI DSS playing a role here?” (Look for 10.x, 8.x, 12.10.5)

🧠 Teach:

> This is not just about tools—it’s about **coordination**, **evidence**, and **control**.

---

## ✏️ **6. Debrief, Reflection & Wrap-Up (15 mins)**

🗣️ Ask teams to answer:

* “What worked well in your incident response?”
* “Where were gaps in access control or communication?”

📘 Reflect Prompt from Workbook:

> “What would you do differently in the incident response process?”

🎓 Key Takeaways:

* Access control isn’t just about restricting access—it’s about **knowing who, when, and why**
* Incident response must be **documented, repeatable, and linked to monitoring**
* **PCI DSS 12.10.5**: Requires IR plans that trigger on anomalies like what you just handled

---

## 📦 Deliverables Recap

| Resource                            | Use Case                           |
| ----------------------------------- | ---------------------------------- |
| `access-control-policy-template.md` | Role mapping and MFA policies      |
| `incident-playbook-v1.md`           | Response guidance, escalation flow |
| Student Workbook – Week 5           | Reflections, simulation notes      |

---

## 📢 Capstone Preview (Week 6)

> “Next week, it’s your turn to design and defend. You’ll bring everything together—architecture, logging, access, and policy—and walk us through your PCI-aware system design.”

---
