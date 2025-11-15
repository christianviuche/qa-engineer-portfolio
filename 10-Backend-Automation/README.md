# 10: Backend & API Automation 

This section covers **Backend Automation**, the process of testing the "server-side" of an application. This is the part of the system that the user *does not see*, but that powers all the functionality.

This primarily involves testing the **API (Application Programming Interface)**, which is the "language" that the frontend (website) uses to talk to the backend (server).

* **Analogy:** If a restaurant is an application, the **Frontend** is the *waiter* and the *menu* you see. The **Backend** is the *kitchen*, where the food is actually made. Backend testing ensures the kitchen (server) can take an order (request) and produce the correct food (response), even without a waiter (UI).
* **Why automate this?** It is *significantly* faster, more stable, and more reliable than frontend (UI) automation.

---

## Key Tools & Frameworks

### API Testing Frameworks

* **REST Assured:**
    * **What:** A powerful Java library for testing REST APIs. It's the industry standard for QA Engineers working in a Java ecosystem.
    * **Use:** Known for its clean, fluent, BDD-style syntax (Given/When/Then) for writing API requests and validating responses.

* **Postman / Newman:**
    * **Postman:** A GUI (graphical interface) tool for *manually* designing, testing, and documenting APIs. It's the #1 tool for API exploration.
    * **Newman:** The command-line *automation* tool for Postman. Newman allows you to run your Postman "collections" (sets of tests) in a CI/CD pipeline.

* **Karate Framework:**
    * **What:** An all-in-one testing framework that combines API automation, mocks, and even basic UI automation.
    * **Use:** Its biggest advantage is that test scripts are written in **Gherkin** (Given/When/Then), making them easy for non-programmers to understand.

* **SoapUI:**
    * **What:** A testing tool focused *primarily* on **SOAP** APIs, though it also supports REST. SOAP is an older, XML-based protocol often used in large enterprise systems (like banking or insurance).
    * **Use:** Used for testing these specific "legacy" or enterprise web services.

### E2E Tools with API Capabilities

*(Note: These tools are primarily for E2E testing but are listed here for their strong backend/API testing features).*

* **Cypress:**
    * **What:** While primarily a Frontend E2E tool, Cypress has *excellent* capabilities for testing APIs directly (`cy.request()`).
    * **Use:** Ideal for "hybrid" tests: you can make an API call to create a user (backend) and then use the UI to log in as that user (frontend), all in one test.

* **Playwright:**
    * **What:** Similar to Cypress, Playwright is a modern E2E (frontend) framework, but it also has powerful API testing features (`request`).
    * **Use:** Allows you to test the API directly to set up "state" (like logging in or creating data) before running your UI tests, making them faster and more stable.
