#  Internship Task 2 – Phishing Email Investigation

##  Task Objective

Analyze a sample phishing email and identify suspicious elements such as spoofed addresses, fake URLs, header anomalies, and manipulation tactics.

---

##  Workflow

1. Collected a phishing email sample (`sample_mail.eml`)
2. Verified sender domain → **spoofed**
3. Analyzed headers using MXToolbox (/header_analysis.png)
4. Checked for spelling/grammar mistakes
5. Documented findings in `analysis.md`

---

##  Repository Contents

| File                     | Description                          |
|--------------------------|--------------------------------------|
| `sample_email.eml` | Raw email file or body text       |
| `analysis.md`            | Detailed phishing analysis           |
| `README.md`              | Task overview (this file)            |
| `screenshots/`           | Optional: email, header, link shots  |

---

## 🔍 Summary of Findings

- Spoofed sender address from a fake banking domain
- DNS header fails (SPF/DKIM failed)
- Fake login link disguised as secure banking
- Use of urgency and threats
- Multiple grammar and spelling issues

---

## 👨‍💻 Author

**Name:** kamalesh  
**Internship Role:** Cybersecurity Intern  
**Date:** June 23, 2025
