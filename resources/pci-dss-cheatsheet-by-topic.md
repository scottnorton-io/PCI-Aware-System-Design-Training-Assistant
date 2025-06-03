# 📄 PCI DSS Cheatsheet by Topic (v4.0.1)

This quick-reference guide maps common system design topics to relevant PCI DSS requirements to assist in cross-referencing during design, documentation, or capstone presentation.

---

## 🔄 CI/CD & Change Control (Req 6.x)

| Requirement | Focus Area                                      |
|-------------|-------------------------------------------------|
| 6.3.1       | Secure coding techniques                        |
| 6.3.2       | Security impact review of changes               |
| 6.3.3       | Sensitive data detection in code repositories   |
| 6.4.1       | Documented change procedures                    |
| 6.4.2       | Impact review of all changes                    |
| 6.4.3       | Approval prior to production deployment         |

---

## 💾 Storage & Encryption (Req 3.x)

| Requirement | Focus Area                                       |
|-------------|--------------------------------------------------|
| 3.1.1       | Limit storage of cardholder data                 |
| 3.2.1       | Do not store sensitive authentication data post-auth |
| 3.3         | Mask PAN when displayed                         |
| 3.4.1       | Strong encryption of PAN                        |
| 3.5.1       | Key management practices                        |

---

## 🔐 Access Control & Identity (Req 7–8)

| Requirement | Focus Area                                        |
|-------------|---------------------------------------------------|
| 7.2.2       | Role-based access control                         |
| 8.2.2       | Password complexity and rotation                  |
| 8.3.1       | Multi-factor authentication for admin/remote use  |
| 8.6.1       | No shared admin credentials                       |

---

## 📜 Logging & Monitoring (Req 10.x)

| Requirement | Focus Area                                       |
|-------------|--------------------------------------------------|
| 10.2.1–10.2.7 | Record access and activity logs                |
| 10.3.1       | Include user ID, timestamp, system component    |
| 10.4.1.1     | Accurate and synchronized time                  |
| 10.5.1       | Protect log integrity                           |
| 10.7.1       | Retain logs for 12 months, 3 months online      |

---

📌 *Use this sheet to validate your evidence matrix and design documentation during capstone or assessment.*