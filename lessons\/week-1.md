This is the **fully detailed Week 1 Instructor Script** for the **PCI-Aware System Design Training Course**.

This script follows the flow of your course structure and integrates practical PCI DSS v4.0.1 references, student prompts, and guided moments to foster discussion.

---

# 🎙️ **Week 1 – Instructor Script**

### Theme: System Design Foundations + PCI Network Architecture (Requirement 1)

---

## 🕘 **Session Duration**: 90 minutes (adjustable)

| Segment                      | Duration | Purpose                                      |
| ---------------------------- | -------- | -------------------------------------------- |
| Opening & Welcome            | 10 mins  | Set tone and expectations                    |
| System Design Concepts Intro | 15 mins  | Explain scalability, latency, and resilience |
| Diagram Walkthrough          | 20 mins  | Visualize architecture layers                |
| PCI DSS Requirement Tie-in   | 15 mins  | Introduce PCI Req 1.2.4                      |
| Exercise + Group Debrief     | 20 mins  | Risk + mitigation at each system layer       |
| Reflection Prompt + Wrap-up  | 10 mins  | Encourage engagement and next steps          |

---

## 🎤 **1. Welcome & Course Kickoff (10 mins)**

> “Welcome everyone to *PCI-Aware System Design*! Over the next six weeks, we’re not just learning how to build secure systems—we’re going to map every technical decision to real-world compliance and business trust.”

* Emphasize **why PCI matters**: It’s not just a checkbox—it’s how we **defend data** and **earn trust**.
* Set **tone**: “This is not a boring compliance course. We’re going to work like architects and defend like assessors.”
* Mention **capstone goal**: “At the end, you’ll design and present your own secure, PCI-aligned system.”

🧭 **Show roadmap:** Display or describe the 6-week curriculum from `📁Addendum: addendum-instructor and student guide.md`

---

## 🧱 **2. System Design 101 – Resilience, Latency & Scale (15 mins)**

> “Let’s start with system design basics—because PCI requirements only make sense when they’re tied to how real systems behave.”

**Topics to define:**

* **Scalability**: How systems grow with user demand.
* **Latency**: Time between request and response.
* **Fault Tolerance**: How systems handle failure gracefully.
* **Tradeoffs**: Why no design is perfect—and what “good enough” means.

🎯 Ask:

> “Who’s worked on a system that scaled beyond what it was designed for?”
> “What was the failure point?”

---

## 🖼️ **3. Architecture Diagram Walkthrough (20 mins)**

Open: `📁Addendum: pci-aware-architecture-v1.png`

Guide them through each component:

* **Developer Workstation**

  > “This is where insecure code is born—or caught early.”

* **CI/CD Pipeline**

  > “This is the software assembly line. We’ll secure this next week.”

* **Load Balancer**

  > “Entry point—must filter and route traffic smartly.”

* **Compute Nodes**

  > “Run the logic. Should be stateless where possible.”

* **Storage**

  > “Where data rests. Encryption, segmentation, and access control come into play.”

* **Logging Layer**

  > “Think of this as our security camera footage—if it’s missing, we can’t explain a breach.”

Prompt:

> “As I go through this diagram, note one thing you *wish* was there—or something that might be a risk.”

---

## 🛡️ **4. PCI DSS Tie-In – Requirement 1.2.4 (15 mins)**

> “Now let’s introduce our compliance hook of the day: PCI DSS Requirement **1.2.4**.”

📎 **Definition**:

* "ADE (Account Data Environment) must be **segmented from untrusted networks**—and this segmentation must be documented."

🧠 Key points:

* **What is the ADE?** – Anywhere CHD/SAD is stored, processed, or transmitted
* **Why segmentation matters** – It’s your **first wall of defense**.
* **Common controls**: firewalls, subnetting, security groups, WAFs

📘 Show:

> How this ties into the “Load Balancer” and “Compute” zones in the architecture diagram.

📢 Ask:

> “Which part of this diagram do you think is most vulnerable to exposure without segmentation?”

---

## 🧪 **5. Exercise – Risk & Mitigation by Layer (20 mins)**

### Instructions:

> “Pair up or work individually. For each system layer from the diagram, write down:
>
> 1. One **potential risk**
> 2. One **mitigation strategy**”

Use a whiteboard, Google Doc, or Jamboard.

| Layer           | Risk Example                      | Mitigation Example                        |
| --------------- | --------------------------------- | ----------------------------------------- |
| Dev Workstation | Unencrypted laptop                | FileVault + remote wipe                   |
| CI/CD           | Secrets exposed in logs           | Use GitHub Actions secrets + redaction    |
| Load Balancer   | Accepts bad traffic from anywhere | IP whitelisting, WAF                      |
| Compute Nodes   | Lateral movement post-exploit     | Run as containers, network ACLs           |
| Storage         | DB left unencrypted               | Transparent Data Encryption + key control |
| Logging         | Logs tampered or deleted          | Centralized WORM logs + access controls   |

After 10 mins, debrief with 2–3 groups sharing insights.

---

## ✏️ **6. Reflection + Wrap-Up (10 mins)**

Prompt (from workbook):

> “Which part of the system is most vulnerable if left unsegmented, and why?”

Have them write in their student workbook or share aloud.

🎓 Closing Lines:

* “Today was about seeing the system like an architect. Next time, we’ll go inside the pipeline—and secure your deployments before a single commit goes live.”
* Encourage: “Review your diagram notes and think like an attacker. Where would *you* sneak in?”

---

## 🧰 Resources Recap:

| File/Artifact                                          | Purpose                                   |
| ------------------------------------------------------ | ----------------------------------------- |
| `pci-aware-architecture-v1.png`                        | Visual system layout for the whole course |
| Student Workbook – Week 1                              | Reflections, exercises, PCI insights      |
| `📁Addendum: addendum-instructor and student guide.md` | Session plan and teaching guide           |

---
