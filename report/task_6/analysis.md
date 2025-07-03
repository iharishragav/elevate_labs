# Password Strength Evaluation and Analysis

## 1. Overview

This document details the evaluation of multiple passwords with varying complexity, using the online tool [How Secure Is My Password?](https://www.security.org/how-secure-is-my-password/). 

The purpose was to:
- Assess strength and time to crack
- Identify best practices for password creation
- Summarize how complexity impacts security

---

## 2. Passwords Tested

| Password Example           | Time to Crack             | Strength Rating         | Tool Feedback                          |
|----------------------------|---------------------------|-------------------------|----------------------------------------|
| password123                | 0 seconds                 | very week               | oh dear using that password is         |
|                            |                           |                         | like leaving your front door wide open |
| Summer2025!                | 1 hour                    | weak                    | using that password is like leaving    |
|                            |                           |                         | your key in lock                       |
| S!7nG@u4^mP                | 2 thousand years          | very strong             | fantastic using that password makes you|
|                            |                           |                         | as secure as fort knox                 |
| #Xr9@2Lq!8e*T7             | 190 billion years         | very strong             | fantastic using that password makes you|
|                            |                           |                         | as secure as fort knox                 | 
| Th!s1s@Sup3rS3cur3P@ss     | 38 years                  | very strong             | fantastic using that password makes you|
|                            |                           |                         | as secure as fort knox                 |

> 📸 *Screenshots are stored in `/screenshots/` directory.*

---

## 3. Key Observations

**Short/weak passwords (e.g., "password123"):**
- Cracked instantly or in seconds
- Common in breaches
- Rated "Very Weak"

**Moderate passwords (e.g., "Summer2025!"):**
- Improved cracking time (1 hrs)
- Still predictable due to dictionary words

**Strong passwords (e.g., "#Xr9@2Lq!8e*T7"):**
- Time to crack extended to decades or centuries
- High entropy
- Rated "Strong" or "Very Strong"

---

## 4. Best Practices Identified

Based on the evaluation and sources consulted:

- Use **at least 12–16 characters**
- Combine **uppercase, lowercase, numbers, symbols**
- Avoid **dictionary words and common patterns**
- Employ **random generation tools**
- Never reuse passwords across accounts
- Enable **multi-factor authentication (MFA)**

---
