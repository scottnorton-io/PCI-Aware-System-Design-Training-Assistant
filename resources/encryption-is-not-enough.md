# 🎙️ Micro-Lecture: Encryption Is Not Enough

Most teams think: “We encrypted the database, we’re good.”  
But PCI DSS says — not so fast.

## 🔐 Key Points

- **Requirement 3.4.1** requires **strong encryption** of PAN and CHD at rest.
- **Requirement 3.5.1** demands that you protect the encryption **keys**, too.
- Encryption only works if:
  - Keys are rotated
  - Keys are stored separately from data
  - Access to keys is limited and logged

## 🎓 Analogy

> “It’s like locking your valuables in a safe, then taping the key to the door.”

## 🧠 Prompt

> “Can you show where keys are stored in your architecture diagram—and who can access them?”

---