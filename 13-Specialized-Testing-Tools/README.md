# 13: Specialized Testing Tools (Non-Functional)

This section covers the tools and frameworks used for **Non-Functional Testing**. These are specialized disciplines that require specific tooling to verify the speed, security, and inclusivity of the application.

---

## 1. Load & Performance Testing ⏱️

Performance testing ensures the system is fast and stable. Load testing ensures it can handle many users at once.

### Key Tools (From Roadmap)

* **JMeter (Apache):**
    * **Type:** The "Classic" Standard. Java-based.
    * **Use:** The most widely used open-source tool for heavy load testing. It simulates thousands of users hitting the server. It has a GUI but is complex.
* **K6:**
    * **Type:** The "Modern" Standard for Devs.
    * **Use:** A developer-centric load testing tool written in Go/JavaScript. You write load tests as code (JS), making it perfect for CI/CD pipelines.
* **Gatling:**
    * **Type:** Scala-based high-performance tool.
    * **Use:** Known for its ability to simulate massive loads with very few resources ("Code as infrastructure").
* **Lighthouse (Google):**
    * **Type:** Frontend Performance.
    * **Use:** Built into Chrome DevTools. It audits the *client-side* speed (Core Web Vitals), SEO, and Best Practices of a specific web page.
* **Locust / Artillery / Vegeta:**
    * **Locust:** Python-based, great for swarm testing.
    * **Artillery:** Node.js-based, great for testing microservices.
    * **Vegeta:** HTTP load testing tool focused on constant request rates.

---

## 2. Security Testing 🔒

Security testing ensures user data is protected. While "Penetration Testing" is a specialized job, QA Engineers perform basic security checks.

### Key Concepts & Areas

* **OWASP Top 10:**
    * Not a tool, but a **document**. It lists the 10 most critical web application security risks (e.g., Injection, Broken Access Control). Every QA must know this list.
* **Authentication vs. Authorization:**
    * **Authentication:** "Who are you?" (Login, Passwords, Secrets Management).
    * **Authorization:** "What are you allowed to do?" (Permissions, Admin vs. User).
* **Vulnerability Scanning:**
    * Automated tools that scan the code or app to find known security holes (like outdated libraries).
* **Attack Vectors:**
    * The paths or means by which a hacker can gain access to a computer or network server.

---

## 3. Accessibility Testing (a11y) ♿

Accessibility (often abbreviated as **a11y**) ensures the software is usable by people with disabilities (vision, hearing, motor).

### Key Tools

* **WAVE (Web Accessibility Evaluation Tool):**
    * A browser extension that visualizes accessibility issues directly on the page (e.g., showing where images are missing "alt" text).
* **AXE (by Deque):**
    * An automated engine for finding accessibility defects. It integrates with Chrome DevTools and automation frameworks like Cypress and Selenium.
* **Chrome DevTools (Lighthouse):**
    * Chrome has a built-in "Accessibility" tab that creates an audit report, giving the site a score from 0 to 100.
