# Security Policy

CollectiVAI works with topics like AI, cybersecurity, blockchain and governance.  
Even though much of the code is experimental and pre-production, **security still matters**.

This document explains how to report security issues responsibly.

---

## Supported scope

At this early stage, most repositories are:

- prototypes,
- lab setups,
- documentation and scripts for personal use.

There is no public “production service” yet.  
Still, we appreciate responsible disclosure for any of the following:

- vulnerabilities in code that could lead to:
  - remote code execution,
  - privilege escalation,
  - data leakage,
  - integrity issues in governance / voting logic (later),
- unsafe default configurations in published examples,
- serious weaknesses in security-related documentation.

---

## Reporting a vulnerability

If you believe you have found a security issue, **do not open a public GitHub issue**.

Instead, please contact:

- 📧 **info@collectivai.org**  
  with subject line: `[SECURITY] <short summary>`

Include, if possible:

- the affected repository and file(s),
- steps to reproduce,
- your environment (OS, version, tools),
- any potential impact you see.

Please give us **reasonable time** to understand and fix the issue before you publish any details.

---

## What to avoid

When researching or reporting security issues, **do not**:

- attempt to access data that clearly does not belong to you,
- perform denial-of-service attacks,
- spam infrastructure or third-party services,
- publicly share exploits before there has been a chance to respond.

---

## Cryptography, blockchain & AI

Some repositories may later involve:

- blockchain nodes (Bitcoin, Ethereum, Cosmos),
- AI routing and prompt handling,
- security and monitoring scripts.

These are often used in **personal lab environments**.  
Please be aware that:

- examples may **not** be secure enough for production,
- node setups may be intentionally simplified,
- cryptographic considerations may still be evolving.

If you see unsafe patterns in public docs or scripts, please report them as well.

---

## Appreciation

Responsible disclosure helps make CollectiVAI safer for everyone –  
from individual users to institutions and public bodies.

Thank you for taking the time to report issues responsibly. 🙏
