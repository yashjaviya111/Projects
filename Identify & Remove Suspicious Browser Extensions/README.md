# Task 7: Identify and Remove Suspicious Browser Extensions

## 📌 Objective

The goal of this task was to inspect the browser environment, analyze all installed extensions for suspicious behavior, evaluate permission scopes, and take action to remove or review those posing risks to user privacy or browser performance.


## 🛠 Tools & Environment

| Component            | Details                                     |
|----------------------|---------------------------------------------|
| Operating System     | Windows 11 Pro                              |
| Browser              | Google Chrome                               |
| Browser Version      | 137.0.7151.56 (Latest Stable)               |
| Analysis Tools       | Chrome Extension Manager, WHOIS Lookup, Task Manager |
| Documentation Tools  | Markdown Editors (Typora, GitHub), Screenshot Tools |


## 🧪 Methodology

1. **Accessed Chrome Extension Manager**
   - Viewed and captured the list of installed extensions via `chrome://extensions/`.

2. **Initial Assessment**
   - Identified each extension.
   - Asked:
     - Do I remember installing this?
     - Have I used this in the last 30 days?

3. **Permission & Behavior Analysis**
   - Reviewed extension details and permission scopes.
   - Verified developer identity via Chrome Web Store and GitHub.

4. **Threat Intelligence & Review**
   - Cross-checked extensions against:
     - User reviews
     - Reddit threads
     - Known CVEs or flagged activities

5. **Action Taken**
   - Removed unused or suspicious extensions.
   - Restarted browser and monitored changes.

6. **Documentation**
   - Maintained logs and screenshots.
   - Compiled a complete report for submission.


## 🔍 Extension Audit Summary

| Extension Name            | Permissions             | Evaluation | Action   | Comments                                      |
|---------------------------|--------------------------|------------|----------|-----------------------------------------------|
| Malwarebytes Browser Guard| Full Access              | Safe       | Kept     | Trusted vendor; anti-scam and phishing tool   |
| Turbo VPN                 | Full Access, Proxy Ctrl  | Suspicious | Removed  | High-risk, logs user traffic, unknown vendor  |
| Wappalyzer                | Site Detection           | Safe       | Kept     | Ethical recon tool                            |
| Copyfish OCR Tool         | Site Content, DOM        | Medium     | Review   | Unused recently, high access for OCR          |
| Read AI – Gmail & Meet    | Event-triggered Access   | Low Risk   | Optional | Minimal access; kept for now                  |


## 📈 Performance Metrics

| Metric               | Before Cleanup | After Cleanup |
|----------------------|----------------|---------------|
| Browser Startup Time | ~4.5 seconds   | ~2.9 seconds  |
| RAM Usage (6 Tabs)   | 1.1 GB         | 870 MB        |
| Extension Count      | 5              | 4             |
| Popups/Redirects     | Occasionally   | None          |

## ⚠️ Real-World Threats Researched

| Threat Type            | Description                                 | Real Incident Example                         |
|------------------------|---------------------------------------------|------------------------------------------------|
| Keylogging             | Capture typed data                          | DataSpii leak exposed sensitive credentials    |
| Redirects              | Modify homepage/search to malicious sites   | QuickSearch Boost redirected to ad sites       |
| Ad Injection           | Embed affiliate ads into pages              | ShoppersTab used for ad manipulation           |
| Background Access      | Operates silently without visibility        | Via `background.js` abuse                      |
| Cross-device Sync Abuse| Spreads via Chrome Sync across accounts     | Exploited via linked account hijacking         |
| Security Header Bypass | Bypass CSP/XFO for XSS injection            | Found in malicious productivity extensions     |


## ✅ Action Log

- [x] Audited all installed extensions
- [x] Removed suspicious VPN extension
- [x] Captured and reviewed screenshots
- [x] Monitored browser memory and CPU
- [x] Documented and submitted report


## 🧠 Conclusion & Reflection

This task reinforced:
- The need for **monthly browser extension audits**
- Applying the **principle of least privilege**
- **Developer reputation verification** before installing
- Awareness that **free extensions** may come at the cost of privacy

> Even legitimate extensions can turn rogue after ownership changes, making ongoing vigilance crucial.

## Author
**Yash Javiya**
