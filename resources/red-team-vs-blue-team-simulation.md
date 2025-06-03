# 🚨 Red Team vs. Blue Team Simulation

**Module:** Week 5 or Week 6  
**Duration:** 30–45 minutes  
**Mode:** Group exercise or live simulation  
**Goal:** Teach rapid PCI DSS mapping and evidence-based defense

---

## 🎮 Scenario Overview

### Red Team Role:
You’re an internal auditor, penetration tester, or rogue insider.  
Your goal is to present a **realistic PCI risk** based on common misconfigurations or lapses.

### Blue Team Role:
You’re the security team defending the design and compliance integrity of the system.  
Your mission: **Defend your design using artifacts and evidence.**

---

## 🔴 Red Team Surprise Scenario

**💣 Incident Trigger:**  
During a CI/CD audit, you find this in a GitHub repo:

```yaml
- name: Deploy to Production
  run: sshpass -p 'SuperSecret123' ssh user@server "deploy.sh"
```

**🔍 Red Team Claim:**  
"This is a **hardcoded credential** in a deployment script. This violates secure coding and secrets management best practices."

**📎 PCI DSS Impact:**

- **6.3.3** – Protect sensitive data in code
- **8.6.1** – No shared or hardcoded credentials
- **10.2.1** – Audit trails must include credential usage

---

## 🔵 Blue Team Response Guidelines

### Step 1: Acknowledge
- Admit the risk **if valid** or refute with context (e.g., "This is dummy code in a non-production repo.")

### Step 2: Defend
- Point to secure CI/CD YAML (`secure-cicd-template-v1.yaml`)
- Show secrets scanning (`trufflehog`, etc.)
- Reference controls in your **Access Control Policy**
- Cite audit logs, GitHub PR templates, and Slack deploy alerts

### Step 3: Map to PCI Requirements
| Requirement | Evidence |
|-------------|----------|
| 6.3.3       | Secrets scanning step in pipeline |
| 8.6.1       | Policy banning shared credentials |
| 10.2.1      | CI logs showing individual user triggering the pipeline |

---

## 💬 Reflection Prompts

- "What signals would have alerted you to this risk in your system?"
- "Where would you surface evidence to refute the Red Team claim?"
- "How would you ensure this never happens again?"

---

## 🧠 Bonus Variations

- 🧨 Red Team injects a **log deletion attempt** (violates 10.5.1)
- 🛡️ Blue Team must respond with centralized WORM logging setup
- 🕵️ Add a **rogue admin user** scenario (Req 7.2.2, 8.3.1, 12.10.5)

---

This simulation encourages **critical thinking**, **evidence fluency**, and **team-based defense strategy** under simulated pressure—just like a real audit.