# 🌐 Web Hacking Basics

Notes derived from TryHackMe's "Introduction to Web Hacking" module.

## 1. Walking An Application
Before using automated tools, manually review the application structure.

* **View Source (`Ctrl+U`):** Look for hidden comments (``), developer notes, or old versions of code.
* **Developer Tools (`F12`):**
    * **Inspector:** Modify HTML client-side to bypass basic checks.
    * **Network Tab:** Monitor requests aimed at the server (API calls, hidden parameters).

## 2. Content Discovery
Techniques to find files and directories not linked on the main page.

### Manual Checks
* `/robots.txt`: Rules for search engine crawlers (often hides admin panels).
* `/sitemap.xml`: List of valid routes on the website.
* **Favicon Database:** Checking the hash of `favicon.ico` against known databases (OWASP database) to identify the framework used.

### Automated Tools
* **Gobuster / Dirb:** Tools used for brute-forcing directory names using wordlists (e.g., `common.txt`).
