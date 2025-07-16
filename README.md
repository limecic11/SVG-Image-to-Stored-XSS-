# SVG-Image-to-Stored-XSS

# 🐾 Stored XSS via SVG Image Upload in Chat Feature

**Author:** [@0xRaccoon](https://medium.com/@0xRaccoon)  
**Write-up:** [Medium Article](https://medium.com/@0xRaccoon/svg-image-to-stored-xss-ce9a4d7839ce)  
**Status:** High severity bug 🔴
**Severity:** High  
**Impact:** Stored XSS → Potential for Cookie Theft, Session Hijack

---

## 📝 Summary

While testing a chat functionality in a web application, I discovered a **Stored XSS** vulnerability through the image upload feature. The platform allowed uploading SVG files without proper sanitization, enabling the injection of malicious JavaScript code.

Although the bug was marked as a **duplicate**, this write-up shares the full discovery process to help others identify and exploit similar issues in real-world applications.

---

## 🔍 Vulnerability Details

- **Vector:** SVG file with embedded JavaScript via alert
- **Injection Point:** Image upload in chat feature
- **Execution:** Triggered when the SVG is rendered in the chat
- **Bypass:** The SVG appeared valid (image loads), but triggers JS silently

---

## 💥 Proof of Concept (POC)

![XSS Screenshot](XSS-PoC.png)
