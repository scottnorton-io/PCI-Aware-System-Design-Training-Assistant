# 📁 addendum-instructor and student guide.md

Title: Course Delivery Aids for PCI-Aware System Design
Purpose: Support instruction and student engagement by providing templates, exercises, and visualization tools aligned with PCI DSS v4.0.1.

---

# 🎓 **Instructor Guide: PCI-Aware System Design Training**

**Audience:** Security engineers, developers, DevOps, PCI professionals
**Format:** 6-week course with modular sessions
**Delivery Modes:** Live instruction, self-paced, or blended
**Reference Addendums:**

* `📁Addendum: addendum-system design artifacts.md`
* `📁Addendum: addendum-compliance-specific evidence and resources.md`
* `📁Addendum: addendum-course delivery aids.md`
* `📁Addendum: pci-v4.0.1-evidence-map.xlsx`
* `📁Addendum: pci-aware-architecture-v1.png`

---

## 🧭 Course Structure Overview

| Week | Theme                            | PCI DSS Focus                | Artifacts/Tools                 |
| ---- | -------------------------------- | ---------------------------- | ------------------------------- |
| 1    | System Design Foundations        | Req 1.x (network security)   | `pci-aware-architecture-v1.png` |
| 2    | CI/CD & Secure Deployments       | Req 6.4.x, 6.3.x             | `secure-cicd-template-v1.yaml`  |
| 3    | Data Storage & Encryption        | Req 3.1.1, 3.4.1             | Student quiz + diagram          |
| 4    | Logging & Monitoring             | Req 10.2–10.7, 12.10.5       | `logging-map-pci10.json`        |
| 5    | Access & Incident Response       | Req 7.2.2, 8.3.1, 12.10.5    | Policy + playbook templates     |
| 6    | Capstone & Evidence Presentation | Full compliance traceability | `pci-v4.0.1-evidence-map.xlsx`  |

---

## 📘 Weekly Breakdown & Teaching Aids

### Week 1: **Intro to System Design + PCI Alignment**

* Use `📁Addendum: pci-aware-architecture-v1.png` to walk through the high-level flow.
* Explain ADE/CDE boundary and Requirement 1 (network segmentation).
* Tie infrastructure decisions to control categories (e.g., traffic flow = Req 1.2.4).

### Week 2: **CI/CD with Security Gates**

* Show `secure-cicd-template-v1.yaml` from `📁Addendum: addendum-system design artifacts.md`.
* Highlight SAST, secrets scanning, and alerting steps.
* Discuss how PCI DSS Req 6.4.3 applies to change tracking and review.

### Week 3: **Encrypted Data Storage**

* Discuss tokenization, encryption-at-rest, and disk volume protection.
* Use CI/storage questions from `quiz-module-ci-storage.txt`.
* Emphasize Req 3.4.1 and secure retention policies.

### Week 4: **Logging & Monitoring**

* Explain log field mapping using `logging-map-pci10.json`.
* Walk through centralized log architecture and Req 10.x.
* Introduce `log-retention-standards.md` as a policy sample.

### Week 5: **Access Control & Incident Response**

* Assign and review `access-control-policy-template.md`.
* Run an incident simulation based on `incident-playbook-v1.md`.
* Discuss how these fulfill Req 7.2.2, 8.3.1, and 12.10.5.

### Week 6: **Capstone Project**

* Students design a PCI-aware system and map artifacts to requirements.
* Reference `pci-v4.0.1-evidence-map.xlsx` as a scoring rubric.
* Deliver a mock presentation to “assessors” (peer groups or instructor).

---

## 🧰 Instructor Tools

* Use the `lesson-plan-outline.md` to stay aligned with objectives.
* Provide editable version of `system-flow-diagram-v1.mmd` for whiteboard sessions.
* Optionally bundle all artifacts into a zip for students.

---

## 🏁 Final Outcomes

Participants will be able to:

* Design and defend a secure, scalable system aligned with PCI DSS v4.0.1
* Map technical decisions to PCI requirements
* Produce documentation and evidence for assessments
* Understand practical tradeoffs in secure architecture

---

Here is the complete **Self-Paced Student Workbook** for the **PCI-Aware System Design Training Course**. It’s designed for independent learners and includes weekly objectives, exercises, reflection prompts, and inline PCI DSS compliance awareness.

---

# 📘 **Self-Paced Student Workbook: PCI-Aware System Design**

**Course Duration:** 6 Weeks
**Delivery Mode:** Independent Study
**Skill Level:** Intermediate → Advanced
**Version:** v1.0
**Instructor Support:** Available upon request
**Artifacts Referenced:**

* `📁Addendum: addendum-system design artifacts.md`
* `📁Addendum: addendum-compliance-specific evidence and resources.md`
* `📁Addendum: addendum-course delivery aids.md`

---

## ✅ How to Use This Workbook

Each week consists of:

* 🎯 Learning Objectives
* 🛠 Hands-On Exercise
* 📎 Compliance Insight
* ✏️ Reflection Prompt

Use the provided artifacts and tools in the addendum files to complete tasks. Save your responses for peer review or instructor feedback.

---

## 📅 Week 1: **System Design Foundations**

### 🎯 Objectives

* Understand key components of scalable systems.
* Learn how PCI DSS defines system boundaries and secure design.

### 🛠 Exercise

* Open `pci-aware-architecture-v1.png`
* Identify each system layer (Dev Workstation → Storage).
* List one risk and one mitigation per layer.

### 📎 PCI Insight

* Requirement **1.2.4** – Document and segment the ADE from public networks.

### ✏️ Reflect

> Which part of the system is most vulnerable if left unsegmented, and why?

---

## 📅 Week 2: **CI/CD & Change Control**

### 🎯 Objectives

* Set up a secure CI/CD pipeline.
* Integrate basic compliance checks.

### 🛠 Exercise

* Load `secure-cicd-template-v1.yaml`.
* Highlight:

  * The static analysis step
  * The secrets scanning step
  * Where change control evidence is captured

### 📎 PCI Insight

* Requirement **6.4.3** – Document and approve changes before deploying.

### ✏️ Reflect

> What’s one additional compliance or security control you would add to this pipeline?

---

## 📅 Week 3: **Data Storage & Encryption**

### 🎯 Objectives

* Understand secure storage of Account Data (AD).
* Explore tokenization and backup strategies.

### 🛠 Exercise

* Review encryption approaches (at-rest vs. tokenization).
* Answer quiz questions in `quiz-module-ci-storage.txt`.

### 📎 PCI Insight

* Requirement **3.4.1** – Encrypt CHD using strong cryptography.

### ✏️ Reflect

> Where should encryption keys be stored, and how should they be protected?

---

## 📅 Week 4: **Logging & Monitoring**

### 🎯 Objectives

* Implement log capture and retention policy.
* Detect and respond to anomalous events.

### 🛠 Exercise

* Open `logging-map-pci10.json`.
* Pick 3 fields and explain what each tells an assessor during an investigation.
* Review `log-retention-standards.md` for best practices.

### 📎 PCI Insight

* Requirement **10.4.1.1** – Ensure logs have accurate, synchronized time.

### ✏️ Reflect

> Why is it important to prevent tampering with logs?

---

## 📅 Week 5: **Access Control & Incident Response**

### 🎯 Objectives

* Apply access role segregation and MFA.
* Follow a tested incident response flow.

### 🛠 Exercise

* Review `access-control-policy-template.md`.
* Simulate an incident using `incident-playbook-v1.md`.
* Identify which steps fulfill PCI DSS Req 12.10.5.

### 📎 PCI Insight

* Requirement **7.2.2** – Roles must match least privilege principle.
* Requirement **12.10.5** – Respond immediately to incidents.

### ✏️ Reflect

> What would you do differently in the incident response process?

---

## 📅 Week 6: **Capstone – System & Compliance Mapping**

### 🎯 Objectives

* Apply everything learned to design and justify a secure system.
* Present compliance evidence aligned to PCI DSS v4.0.1.

### 🛠 Exercise

* Reuse `pci-aware-architecture-v1.png` and annotate it with:

  * Log paths
  * Encryption points
  * Access roles
  * Incident triggers

* Use `pci-v4.0.1-evidence-map.xlsx` to complete your requirement coverage checklist.

### 📎 PCI Insight

* Use real sub-requirements as headings to guide your documentation.

### ✏️ Reflect

> Which compliance requirements felt “natural” to satisfy through good design, and which felt like bolt-ons?

---

## 📦 Submission Checklist (Optional)

* [ ] Architecture Diagram (Annotated)
* [ ] CI/CD YAML with inline comments
* [ ] Access Policy Document
* [ ] Incident Runbook Response
* [ ] Completed Evidence Mapping Sheet
* [ ] One-page Reflection Summary

---
