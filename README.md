# DVWA Security Testing Walkthrough

**Author:** Masum Ansari  
**Project type:** Educational web application security lab  
**Target:** Damn Vulnerable Web Application (DVWA)

## Overview

This repository contains a screenshot-based walkthrough of common web application vulnerabilities demonstrated in DVWA, an intentionally vulnerable training application. It is intended to document learning and hands-on practice, not to represent a client engagement or a production penetration test.

### Topics covered

- Brute-force testing
- OS command injection
- File inclusion and path traversal concepts
- Blind SQL injection
- SQL injection
- File-upload validation weaknesses
- Cross-Site Request Forgery (CSRF)
- Stored Cross-Site Scripting (XSS)
- Reflected Cross-Site Scripting (XSS)

Tools shown in the walkthrough include Burp Suite and sqlmap.

## Repository contents

- `DVWA_Security_Testing_Walkthrough.pdf` — original walkthrough with an updated cover page and author attribution.
- `Portfolio_Quality_Review_and_Remediation.pdf` — executive summary, scope, evidence-based findings overview, defensive remediation guidance, limitations, and publishing notes.

## How to use this project

1. Read the walkthrough alongside the remediation addendum.
2. Reproduce examples only in your own local DVWA lab or another explicitly authorized environment.
3. Treat screenshots as evidence of the documented lab exercise; they are not independent verification of a real-world application.
4. Use the remediation guidance to understand how developers can reduce the risks.

## Scope and limitations

The report documents an educational DVWA environment. It is not a formal client penetration-test report, and the examples have not been independently retested as part of preparing this repository. Any severity labels in the addendum are indicative learning priorities, not CVSS scores or production risk ratings.

The original walkthrough includes environment-specific local addresses, session examples, and tool-interface details that may be outdated. Review all screenshots and commands before publishing. Do not include live secrets, valid credentials, or data from systems you do not own or have permission to test.

## Defensive takeaways

- Use parameterized SQL queries rather than concatenating user input.
- Avoid shell execution with untrusted input.
- Apply robust file-upload validation and store uploaded files safely.
- Encode untrusted output in the correct HTML/JavaScript context to prevent XSS.
- Protect state-changing requests against CSRF with anti-CSRF tokens and suitable cookie controls.
- Apply rate limiting, MFA, and monitoring to reduce brute-force risk.

## Responsible use

This repository is for education and authorized security testing only. Do not use the techniques described here against systems without explicit permission.

## Suggested future improvements

- Proofread the original walkthrough and correct terminology.
- Add consistent captions and finding IDs to the screenshots.
- Add a reproducibility section with the DVWA version and lab configuration used.
- Re-test every demonstration in a local lab before stating that it is reproducible.
- Include remediation evidence after applying fixes, where the lab supports it.
