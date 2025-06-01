# Developer Workstation Hardening Guide

## Overview
Secure setup and operation of developer workstations is essential to PCI DSS compliance and organizational security.

## Hardening Checklist

- ✅ Use encrypted disk volumes (FileVault/BitLocker)
- ✅ Install antivirus and configure auto-updates
- ✅ Run a local firewall (Little Snitch/UFW)
- ✅ Configure static code analysis in the IDE
- ✅ Block USB ports unless explicitly authorized
- ✅ Restrict terminal access to authorized shells
- ✅ Use password managers for credential storage
- ✅ Rotate SSH keys every 90 days
- ✅ Enable full-disk logging of local code scans

## PCI DSS Relevance
- **6.2.4** – Enforce secure coding practices
- **6.3.1** – Use of code review tools
- **6.3.3** – Detect and manage sensitive data