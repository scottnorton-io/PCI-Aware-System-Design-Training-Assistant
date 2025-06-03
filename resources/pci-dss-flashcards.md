# 🧠 PCI DSS Flashcards – System Design Edition

---

## 🔐 PCI Requirement Definitions

**Q:** What does PCI DSS Requirement 6.4.3 require?  
**A:** That all changes to production systems are approved prior to implementation.

**Q:** What is the purpose of Requirement 3.4.1?  
**A:** To ensure PAN is rendered unreadable anywhere it is stored using strong encryption.

**Q:** What is Requirement 8.3.1 focused on?  
**A:** Enforcing multi-factor authentication for all remote and administrative access.

**Q:** What does Requirement 10.5.1 address?  
**A:** Protecting audit logs from unauthorized modification.

**Q:** What does Requirement 12.10.5 require?  
**A:** Immediate response to alerts indicating potential compromise.

---

## 📁 Artifact-to-Requirement Matching

**Q:** Which artifact supports compliance with Requirement 6.3.3?  
**A:** `secure-cicd-template-v1.yaml` — includes secrets scanning via trufflehog.

**Q:** What document maps to Requirement 7.2.2 (RBAC)?  
**A:** `access-control-policy-template.md` — outlines role-based access control.

**Q:** Which file helps demonstrate compliance with log integrity (10.5.1)?  
**A:** `log-retention-standards.md` — includes tamper protections like WORM storage.

**Q:** Which artifact is evidence for Requirement 12.10.5?  
**A:** `incident-playbook-v1.md` — documents detection, escalation, and recovery steps.

**Q:** What shows alignment with Requirement 6.4.1?  
**A:** Pull request records + `secure-cicd-template-v1.yaml` with change steps.

---

Use these flashcards to reinforce your command of PCI DSS requirements and their application in system design. Ideal for Anki/Quizlet import or live quiz rounds.