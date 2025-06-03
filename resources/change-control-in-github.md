# 🎙️ Micro-Lecture: What Does 'Change Control' Look Like in GitHub?

Change control isn’t just a checkbox—it’s how you defend your production environment from careless mistakes or malicious commits.

## 🔄 PCI Connection

- Requirement **6.4.1–6.4.3** mandates:
  - Documented changes
  - Impact review
  - Approval before deployment

## ✅ Real-World Application in GitHub

- Every Pull Request (PR) is a **change record**.
- PR descriptions can include risk assessments or change impact.
- Review approvals = **change authorization**
- GitHub Actions workflows tied to `main` branch enforce gated deployments.
- Logs from CI tools or Slack notifications show **deployment history**.

## 🧠 Thought Prompt

> “Could you walk an assessor through your last 3 deployments using GitHub PRs and CI logs? If yes—you’re audit-ready.”

---