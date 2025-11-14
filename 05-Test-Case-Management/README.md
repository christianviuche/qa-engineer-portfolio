# 05: Test Case Management (TCM) Tools

While Project Management tools (like Jira, from Section 04) are used to track bugs and user stories, a **Test Case Management (TCM)** tool is a specialized platform used to *design, organize, and execute* test cases.

For a QA Engineer, the TCM tool is our primary workbench for:
* **Writing Test Cases:** Authoring step-by-step test instructions.
* **Organizing Test Suites:** Grouping tests into logical sets (e.g., "Login Tests," "Regression Suite").
* **Executing Test Runs:** Going through tests one by one and marking them as Pass, Fail, or Blocked.
* **Tracking Results & Reporting:** Creating dashboards and reports that show testing progress and defect rates.

---

## The Jira Connection (Critical)

Many modern TCM tools are not standalone platforms; they are **plugins that integrate directly into Jira**. This is the key relationship between Section 04 and Section 05.

* **You track the User Story in Jira.**
* **You write/link the Test Cases in the TCM tool (e.g., Zephyr).**
* **You report the Bug in Jira.**
* The TCM plugin then links all three (Story ↔ Test Case ↔ Bug) together.

---

## Key Tools & Platforms

### 1. Zephyr (by SmartBear)

**Zephyr** is one of the most popular TCM solutions *specifically because* it lives inside Jira as a native plugin.

* **Core Use:** Allows you to create "Test" issues directly inside your Jira project. You can link tests to stories, group them into test cycles, and execute them all without leaving Jira.

### 2. TestRail

**TestRail** is a powerful and widely-used *standalone* TCM tool. It is often used *alongside* Jira, not inside it.

* **Core Use:** It's a dedicated, web-based platform for managing all test cases, suites, and plans. It has robust reporting and integrates well with Jira (i.e., you can push a bug report from TestRail to Jira), but it is its own separate application.

### 3. qTest

**qTest** is an enterprise-level test management tool. It's a heavy-duty, scalable solution for large organizations.

* **Core Use:** Like TestRail, it's a standalone platform that integrates with Jira. It's known for its powerful features, including requirements management and integration with automation tools.

### 4. TestLink

**TestLink** is a popular **open-source** and web-based TCM tool.

* **Core Use:** It's a free alternative to paid tools like TestRail. While its interface may not be as modern, it's a very functional tool for organizing test suites, creating test plans, and tracking execution.
