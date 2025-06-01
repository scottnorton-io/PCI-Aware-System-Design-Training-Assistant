### 📁 `addendum-compliance-specific evidence and resources.md`

**Title:** Compliance-Specific Evidence & PCI Resource Addendums
**Purpose:** Provide modular, PCI DSS-aligned evidence templates and standards that support the system design training course.

---

## 🔐 Compliance Support Files

| Filename                            | File Type   | Description                                                              | PCI DSS Relevance                                      |
| ----------------------------------- | ----------- | ------------------------------------------------------------------------ | ------------------------------------------------------ |
| `pci-v4.0.1-evidence-map.xlsx`      | Spreadsheet | Mapping matrix aligning system artifacts to PCI DSS v4.0.1 requirements. | Full cross-reference aid for all PCI sub-requirements. |
| `access-control-policy-template.md` | Markdown    | Template for role-based access, 2FA, and user provisioning policies.     | Req **7.2.2**, **8.3.1**, **8.6.1**                    |
| `incident-playbook-v1.md`           | Markdown    | Incident response plan with Slack/PagerDuty triggers and escalation.     | Req **12.10.5**                                        |
| `log-retention-standards.md`        | Markdown    | Secure log lifecycle and retention policy.                               | Req **10.3.1–10.7.1**, **10.5.1**                      |

---

### 📑 `access-control-policy-template.md`

```markdown
# Access Control Policy Template

## Purpose
To restrict logical access to systems and data to authorized individuals.

## Roles
- Administrator
- Developer
- Read-only Auditor

## Controls
- Role-based access enforcement
- MFA required for all interactive access
- Access reviews performed quarterly
- Unique IDs assigned to all users

## PCI DSS Alignment
- **7.2.2** – Role assignment tied to business need
- **8.3.1** – MFA for all remote and admin access
- **8.6.1** – No shared credentials for admin access
```

---

### 📑 `incident-playbook-v1.md`

```markdown
# Incident Response Playbook

## Phase 1 – Detection
- Monitor alerts from WAF, IDS, log aggregator
- Slack bot notification to #security-channel
- Trigger PagerDuty escalation if severity ≥ medium

## Phase 2 – Containment
- Isolate impacted container or server
- Rotate credentials

## Phase 3 – Notification
- File internal incident ticket
- Notify Compliance Officer

## Phase 4 – Recovery
- Deploy backup image
- Confirm logs captured and archived

## PCI DSS Linkage
- **12.10.5** – Respond immediately to suspected compromise
```

---

### 📑 `log-retention-standards.md`

```markdown
# Logging and Retention Standards

## Retention Periods
- Security logs: 1 year minimum
- Application logs: 90 days
- Authentication logs: 12 months

## Protection Mechanisms
- Write-once storage
- Hash-based integrity checks
- Centralized logging with access controls

## PCI DSS Coverage
- **10.3.1** – Capture user IDs and timestamps
- **10.5.1** – Protect logs from unauthorized changes
- **10.7.1** – Store logs ≥12 months, 3 months readily available
```

---

> 📌 *Note: `pci-v4.0.1-evidence-map.xlsx` must be uploaded as a standalone spreadsheet addendum. It provides essential traceability between course artifacts and PCI DSS testing procedures.*

