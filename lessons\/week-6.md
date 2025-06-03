This is the **fully detailed Week 6 Instructor Script** for the **PCI-Aware System Design Training Course**, featuring final presentations, system design defense, and compliance traceability.

---

# 🎙️ **Week 6 – Instructor Script**

### Theme: Capstone Presentation & PCI DSS Mapping

📌 **PCI DSS Focus**: All relevant sub-requirements from Weeks 1–5

---

## 🕘 **Session Duration**: 90–120 minutes (adjustable for group size)

| Segment                          | Duration   | Purpose                                                   |
| -------------------------------- | ---------- | --------------------------------------------------------- |
| Welcome & Final Prep             | 10 mins    | Set tone, recap the journey, explain the scoring approach |
| Student Presentations (Capstone) | 60–90 mins | Teams/individuals present designs & walk through controls |
| Feedback & Q\&A                  | Embedded   | Real-time or end-of-presentation engagement               |
| Peer Scoring + Group Debrief     | 10–15 mins | Discuss what was learned, see design differences          |
| Final Reflection & Wrap-Up       | 10–15 mins | Celebrate outcomes, prompt next steps, course closeout    |

---

## 🎤 **1. Welcome & Final Prep (10 mins)**

🎤 Say:

> “Today, you become the architects, engineers, and defenders. This is your moment to show how compliance isn’t separate from good design—it’s baked in.”

Set tone:

* This is **not a test** — it’s a demonstration of understanding and intentionality.
* Emphasize that clear **rationale** and **control traceability** matter more than perfection.

📋 Display or distribute:

* Presentation checklist from the workbook
* Evidence scoring criteria from `📁Addendum: pci-v4.0.1-evidence-map.xlsx`

---

## 🧑‍🏫 **2. Student Presentations (60–90 mins)**

🎯 Each student/team should:

### Required Elements:

1. **Show their architecture**
   (Annotated `pci-aware-architecture-v1.png` or original diagram)

2. **Describe how each layer is secured**
   (Dev → CI/CD → Load Balancer → Compute → Storage → Logging)

3. **Call out PCI DSS tie-ins by requirement**
   (e.g., “Here’s how we meet 3.4.1 with encryption at rest”)

4. **Share supporting artifacts**:

   * CI/CD YAML w/ inline controls
   * Access Control snapshot or policy snippet
   * Logging policy reference
   * Incident response summary

### Optional:

* Call out **tradeoffs** made
* Mention what they would **do differently next time**

🕐 Suggested time per team:

* 7–10 mins per individual
* 10–15 mins per team

📢 Encourage:

> “Tell us your **design logic** — not just what you built, but *why* you built it that way.”

---

## 👂 **3. Feedback & Q\&A (Embedded)**

After each presentation, use 2–3 minutes for feedback:

* Ask clarifying questions like:

  * “How would you demonstrate change control to an assessor?”
  * “Where do you log failed login attempts?”
  * “How does your tokenization vault reduce PCI scope?”

* Invite peer feedback:

  > “What stood out to you from this design?”

---

## 📋 **4. Peer Scoring + Group Debrief (10–15 mins)**

Distribute or display a simplified **peer scoring card**, focusing on:

| Area                    | Score (1–5) | Notes                            |
| ----------------------- | ----------- | -------------------------------- |
| Architecture Clarity    |             |                                  |
| PCI Requirement Mapping |             | Named and accurate tie-ins?      |
| Artifact Quality        |             | Were templates/evidence present? |
| Incident Readiness      |             | Clear playbook or response flow? |

🧠 Group Discussion Prompts:

> “Which control was most often overlooked?”
> “What design made the best case for built-in compliance?”

---

## ✏️ **5. Final Reflection & Wrap-Up (10–15 mins)**

📘 Reflect Prompt from Workbook:

> “Which compliance requirements felt ‘natural’ to satisfy through good design, and which felt like bolt-ons?”

📢 Ask:

> “How has your thinking changed around PCI DSS since Week 1?”

🎓 Closing Statements:

* Celebrate the work: “You’ve just completed a PCI-aware architecture project from design to defense.”
* Emphasize practical value: “This isn’t just training—it’s how real teams pass audits and build trust.”

---

## 🧰 Deliverables Recap

| Deliverable                          | Purpose                                   |
| ------------------------------------ | ----------------------------------------- |
| Annotated architecture diagram       | Visual explanation of system design       |
| CI/CD YAML with inline PCI refs      | Evidence for Req 6.4.1–6.4.3              |
| Access control policy or summary     | Roles, MFA, unique IDs (Req 7.2.2, 8.3.1) |
| Logging and retention policy snippet | Req 10.x and 12.10.5 compliance           |
| Incident response plan or summary    | Breach readiness, mapped to 12.10.5       |
| Evidence map scorecard               | Used for instructor/peer scoring          |

---

## 🎯 Optional Follow-Up

Would you like:

* A **certificate of completion template**?
* Export of all student artifacts and workbook reflections as a zipped portfolio?
* A feedback form for course evaluation?

And with that... **congratulations on completing the course!**
