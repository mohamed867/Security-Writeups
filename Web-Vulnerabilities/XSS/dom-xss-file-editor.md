# DOM-Based Cross-Site Scripting (XSS) in Web File Editor Parameter

## 📌 Summary
A DOM-Based Cross-Site Scripting (XSS) vulnerability was identified in the web application's file editor interface. Improper sanitization of a URL query parameter allows untrusted input to be dynamically written into the Document Object Model (DOM), resulting in arbitrary JavaScript execution within the victim's browser session.

---

## 🔍 Vulnerability Details
* **Vulnerability Type:** DOM-Based Cross-Site Scripting (CWE-79)
* **OWASP Top 10 Category:** A03:2021 – Injection
* **Severity:** Low
* **Affected Component:** File Editor View (`file` URL parameter)
* **Authentication Required:** Yes (Standard User)

---

## 🛠️ Steps to Reproduce

1. Log in to the application and navigate to the file editor endpoint:
   ```text
   [https://target-application.example/editor?file=document.txt](https://target-application.example/editor?file=document.txt)
