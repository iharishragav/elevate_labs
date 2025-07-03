# Phishing Email Analysis Report

## 1. Sender Spoofing
- **Email Display Name**: Microsoft account team
- **Actual From**: no-reply@access-accsecurity.com
- **Header Domain**: access-accsecurity.com (Suspicious; not an official Microsoft domain)
- **Return Path**: bounce@thcultarfdes.co.uk
- **Verdict**: Spoofed sender identity – typical phishing trait

---

## 2. Email Header Discrepancies
- **SPF Check**: None (domain didn’t authorize sending server)
- **DKIM**: None (email not digitally signed)
- **DMARC**: Permerror (policy error in domain configuration)
- **Verdict**: Authentication failures highly indicative of phishing


---

## 3. Suspicious Links and Tracking
- **All Links Redirect to**: `mailto:sotrecognizd@gmail.com`
- **Tracking Pixel**: `http://thebandalisty.com/track/...`
- **Verdict**: Links intended to harvest responses; tracking pixel suggests click-tracking



---

## 4. Urgency and Threat Language
- Phrases like “Unusual sign-in activity”, “Report the user”, and “If this wasn’t you...”
- Capitalization and immediate call to action (CTA)
- **Verdict**: Psychological manipulation to induce fear and click response


---

## 5. URL and Domain Mismatch
- **Domain Posed As**: Microsoft
- **Actual Domains Used**:
  - `access-accsecurity.com`
  - `thcultarfdes.co.uk`
  - `thebandalisty.com` (for tracking)
- **Verdict**: Clear URL spoofing attempt

---

## 6. Grammar and Language Issues
- Typos: “sign.in” instead of “sign-in”
- Awkward phrasing: “please report the user” in CTA format
- **Verdict**: Indicates non-professional origin, likely from phishing kits

---

## 7. Attachments/Size Irregularity
- **Content-Lengths**: `18708448`, `1821750` – huge sizes with no real attachment visible
- **Verdict**: Bloating to evade spam filters or include hidden scripts

---

## 8. Summary of Phishing Traits
| Trait                           | Evidence                                     |
|--------------------------------|----------------------------------------------|
| Spoofed Sender Address         | `no-reply@access-accsecurity.com`            |
| SPF/DKIM/DMARC Failures        | `None`, `Permerror`                          |
| Urgent / Threatening Language  | “Report the user”, “Unusual sign-in”         |
| Mismatched Domains/URLs        | Discrepant domain impersonation              |
| Suspicious Links               | `mailto:sotrecognizd@gmail.com`              |
| Grammar Errors                 | “sign.in”, odd phrasings                     |
| Tracking Pixel                 | `http://thebandalisty.com/track/...`         |

> **Conclusion**: High-confidence phishing attempt.

