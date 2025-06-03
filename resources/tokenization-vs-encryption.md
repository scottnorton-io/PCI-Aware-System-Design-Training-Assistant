# 🎙️ Micro-Lecture: Tokenization vs. Encryption

Both protect data—but they work differently and have different PCI scope impacts.

## 🪙 Tokenization

- Replaces sensitive data with **non-sensitive tokens**
- Original data lives in a **secure vault**
- Great for reducing PCI DSS scope (if done before storage)

## 🔐 Encryption

- Uses math (cryptography) to make data unreadable without a key
- PAN is encrypted at rest or in transit
- PCI still applies to encrypted data unless tokenized pre-storage

## ⚖️ PCI Comparison

| Approach     | Requirement | PCI Scope? |
|--------------|-------------|------------|
| Encryption   | 3.4.1       | ✅ Yes     |
| Tokenization | 3.4.1       | ❌ (if before storage) |

📘 PCI DSS doesn’t care which you use—**as long as you implement controls properly**.

---