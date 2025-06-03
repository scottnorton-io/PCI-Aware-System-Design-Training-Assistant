This is the **fully detailed Week 3 Instructor Script** for the **PCI-Aware System Design Training Course**, centered on **Data Storage & Encryption**.

---

# 🎙️ **Week 3 – Instructor Script**

### Theme: Protecting Data at Rest with Encryption & Tokenization

📌 **PCI DSS Focus**: Requirements **3.1.1**, **3.4.1**, **3.5.1**

---

## 🕘 **Session Duration**: 90 minutes (adjustable)

| Segment                             | Duration | Purpose                                             |
| ----------------------------------- | -------- | --------------------------------------------------- |
| Warm-Up Quiz                        | 10 mins  | Reinforce change control and secure coding concepts |
| Intro to Data Security Concepts     | 15 mins  | Frame the risks and goals of storing sensitive data |
| Encryption & Tokenization Deep Dive | 20 mins  | Compare storage protection strategies               |
| PCI DSS Requirement Mapping         | 15 mins  | Tie technical protections to 3.1.1, 3.4.1, 3.5.1    |
| Quiz & Group Exercise               | 20 mins  | CI/CD + Storage questions + design walkthrough      |
| Reflection & Wrap-Up                | 10 mins  | Reinforce tradeoffs, preview logging next           |

---

## 🎤 **1. Warm-Up Quiz (10 mins)**

> “Welcome back! Before we dive in—let’s do a quick pulse check on what we covered around secure deployments.”

**Use from `📁Addendum: quiz-module-ci-storage.txt`**

* Q2: *Which is a good practice in CI/CD?*
* Q4: *True/False – Change control is only required if a rollback fails.*

🧠 **Review Together**:

* Talk through why static analysis and secrets scanning matter.
* Reinforce that **change control applies always**, not just during incidents.

---

## 🔐 **2. Intro to Data Security Concepts (15 mins)**

🎤 Say:

> “Let’s zoom in now on what we’re protecting—**Account Data**. That includes **Cardholder Data (CHD)** and **Sensitive Authentication Data (SAD)**. The #1 goal is to prevent that data from leaking, at rest or in transit.”

Key Concepts:

* **PAN**, **expiration**, and **CVV** rules
* **Data lifecycle**: collected → stored → accessed → purged
* **Threats**: unauthorized access, theft, backup exposure

📢 Ask:

> “Who’s worked in an environment where production DBs were copied into test environments? What controls were in place?”

---

## 🧪 **3. Encryption & Tokenization Deep Dive (20 mins)**

### 🧊 **Encryption at Rest**

* Uses strong cryptography to protect stored data
* AES-256 is the gold standard
* Full-disk vs. column-level encryption
* **Key management is everything**

### 🧪 **Tokenization**

* Replaces sensitive values with tokens
* The real data is stored in a **token vault**
* Ideal for offloading PCI scope if done correctly

📘 Diagram Reference:
Use annotated section of `pci-aware-architecture-v1.png` to highlight the **storage layer** and where encryption/tokenization fits

📢 Ask:

> “If you use tokenization, does your storage still have to be encrypted?”

🧠 Teach:

> Yes—PCI DSS **still requires strong cryptography even if data is tokenized, unless you tokenize before storage**.

---

## 📎 **4. PCI DSS Requirement Mapping (15 mins)**

| Requirement | Meaning                                       | Design Impact                                   |
| ----------- | --------------------------------------------- | ----------------------------------------------- |
| **3.1.1**   | Inventory and limit retention of account data | Apply retention tags, minimize stored fields    |
| **3.4.1**   | Use strong encryption for PAN and CHD         | Encrypt at rest using FIPS-validated algorithms |
| **3.5.1**   | Protect and manage encryption keys securely   | Use HSMs, key rotation, restricted access       |

🧩 Link this back to their system diagram:

> “If assessors ask, ‘Where is encryption applied?’—you should point to your data layer **and** your key management system.”

---

## 🧠 **5. Quiz & Group Exercise (20 mins)**

### Instructions:

1. **Quiz Q1 from `quiz-module-ci-storage.txt`**:
   *“What PCI DSS requirement covers secure storage of PAN?” → Answer: **A) 3.4.1***

2. **Open Group Design Task**:

   > “Draw or annotate a mini architecture that includes:
   >
   > * Encrypted DB
   > * Token vault (if used)
   > * Backup location
   > * Key management system”

Have teams annotate:

* Where keys are stored
* What encryption is used (full-disk, column)
* What PCI requirements are covered

🧠 Shareback:

> “What’s one improvement you’d recommend for storing or managing data securely?”

---

## ✏️ **6. Wrap-Up & Reflection (10 mins)**

📘 Reflect Prompt from Student Workbook:

> “Where should encryption keys be stored, and how should they be protected?”

Encourage written answers or callouts. Then summarize:

🎓 Takeaways:

* **Encrypt everything** storing PAN—even logs or backups.
* **Key control is a compliance hot zone**. If you lose key control, encryption becomes meaningless.
* **Tokenization reduces scope**, but doesn’t remove PCI responsibilities entirely.

---

## 🧰 Deliverables Recap

| Resource                        | Use                             |
| ------------------------------- | ------------------------------- |
| `pci-aware-architecture-v1.png` | Storage layer walkthrough       |
| `quiz-module-ci-storage.txt`    | Assessment and review questions |
| Student Workbook – Week 3       | Objectives, quiz, reflection    |

---

## 📢 Preview Week 4:

> “Next time, we’ll follow the logs. We’ll look at what’s recorded, how to detect incidents, and how logging ties to accountability and incident response.”

---

Would you like this script exported to PDF or paired with a live worksheet + diagram annotation guide? I can also prep slides or a whiteboard version for interactive sessions.
