This is the **fully detailed Week 2 Instructor Script** for the **PCI-Aware System Design Training Course**, focused on CI/CD pipelines and PCI DSS change control alignment.

---

# 🎙️ **Week 2 – Instructor Script**

### Theme: CI/CD & Secure Deployments

📌 **PCI DSS Focus**: Requirements **6.4.1–6.4.3**, **6.3.1–6.3.3**

---

## 🕘 **Session Duration**: 90 minutes (adjustable)

| Segment                             | Duration | Purpose                                        |
| ----------------------------------- | -------- | ---------------------------------------------- |
| Warm-up Review                      | 10 mins  | Reinforce system concepts from Week 1           |
| Intro to Secure CI/CD Concepts      | 15 mins  | CI/CD, pipeline stages, security gate concepts |
| Walkthrough of Secure Pipeline YAML | 20 mins  | Analyze `secure-cicd-template-v1.yaml`         |
| PCI DSS Tie-In                      | 15 mins  | Map pipeline steps to PCI Requirements 6.4.x   |
| Hands-On Group Exercise             | 20 mins  | Annotate pipeline, identify improvement areas  |
| Wrap-Up & Reflection                | 10 mins  | Thought prompt + Week 3 teaser                 |

---

## 🎤 **1. Warm-Up Review (10 mins)**

> “Last session, we mapped out the foundation—your system’s layout and where segmentation matters most. Who remembers what Requirement **1.2.4** mandates?”

* Call on 1–2 students to recap the **Account Data Environment (ADE)** concept.
* Invite quick shares of where they saw **risk** in their architecture from Week 1.

🪄 Transition:

> “Today, we zoom into your software factory: the CI/CD pipeline. If this breaks down, bad code hits production fast—and PCI gets very unhappy.”

---

## 🛠️ **2. Secure CI/CD Overview (15 mins)**

Introduce key terms:

* **CI/CD Pipeline** = Code → Build → Test → Deploy
* **SAST** = Static Application Security Testing
* **Secrets Scanning** = Detecting API keys or credentials
* **Change Control** = Documenting and approving changes

🧠 Teaching Prompt:

> “Security gates are like brakes on a car—not there to slow you down, but to let you go faster… safely.”

📢 Ask:

> “What tools or platforms do you currently use for CI/CD—GitHub Actions? Jenkins? GitLab CI?”

---

## 🔍 **3. Walkthrough: Secure Pipeline YAML (20 mins)**

Open: `📁Addendum: addendum-system design artifacts.md → secure-cicd-template-v1.yaml`

### Step-by-step callout:

```yaml
- name: Run Static Analysis (SAST)
  uses: github/codeql-action/init@v2
```

🎤 Say:

> “This satisfies **PCI DSS 6.3.1** — code review tools and secure coding techniques.”

---

```yaml
- name: Run Secrets Scan
  uses: trufflesecurity/trufflehog@v3
```

🎤 Say:

> “This helps with **6.3.3** — making sure sensitive data (like hardcoded keys) aren’t accidentally pushed to the repo.”

---

```yaml
- name: Deploy to Staging
  if: github.ref == 'refs/heads/main'
  run: ./scripts/deploy-staging.sh
```

🎤 Say:

> “Deployment gating with conditionals supports **6.4.1–6.4.3** — document, approve, and validate changes before pushing to production.”

---

```yaml
- name: Notify Security Team
  run: curl -X POST -H 'Content-type: application/json' ...
```

🎤 Say:

> “Notifications like this serve **operational transparency** and create an audit trail—very helpful for Req **6.4.3**.”

---

## 📋 **4. PCI DSS Tie-In (15 mins)**

🧩 Map CI/CD pipeline steps to key sub-requirements:

| PCI Requirement | What It Requires                        | Covered By YAML                       |
| --------------- | --------------------------------------- | ------------------------------------- |
| **6.3.1**       | Secure coding techniques & code reviews | `Run Static Analysis (SAST)`          |
| **6.3.3**       | Protection of sensitive data in code    | `Run Secrets Scan`                    |
| **6.4.1**       | Documented change processes             | YAML steps + version control          |
| **6.4.2**       | Impact review of changes                | Optional PR templates, staged deploys |
| **6.4.3**       | Approval of changes before production   | Manual approval gates or Slack notify |

📢 Ask:

> “Which of these requirements do you think teams skip the most—and why?”

---

## ✍️ **5. Hands-On Group Exercise (20 mins)**

### Task:

> “In your teams, highlight the following in the YAML file:
>
> 1. Which lines satisfy **PCI DSS 6.4.x**?
> 2. What **evidence** would you collect to show an assessor?
> 3. What one additional control would you add?”

Distribute printouts or use shared online editor (e.g., codeshare, HackMD).

🧠 Examples of evidence:

* PR approval logs
* Static analysis reports
* Git commit history
* Slack notifications from deployments

After 10–12 mins, invite groups to share 1 insight or improvement.

---

## ✏️ **6. Wrap-Up & Reflect (10 mins)**

🎓 Prompt from the workbook:

> “What’s one additional compliance or security control you would add to this pipeline?”

📘 Let students record their answer in their **Week 2 section of the workbook** or share aloud.

---

## 🎁 **Week 2 Deliverables Recap**

| Resource                             | Description                             |
| ------------------------------------ | --------------------------------------- |
| `secure-cicd-template-v1.yaml`       | Annotated secure CI/CD flow             |
| Week 2 Workbook Page                 | Objectives, reflection, YAML annotation |
| `quiz-module-ci-storage.txt` Q2 & Q4 | Good pop quiz warm-up for next time     |

---

## 📢 Preview Week 3:

> “Next session, we dig into **data storage and encryption**—we’ll talk about how to protect what attackers actually want: cardholder data.”

---

Would you like this Week 2 script exported as a PDF, or bundled with slides and YAML annotations? Ready when you are!
