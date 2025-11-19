
# 09: Manual Testing Fundamentals 

**Manual Testing** is the process of testing software by *human* interaction. It is a formal process where a QA Engineer acts as the end-user, following a plan to find defects and verify that the application meets its requirements.

Even in an automated world, manual testing is irreplaceable for activities like exploratory testing, usability testing, and for applying the human "QA Mindset" to complex scenarios.

This section covers the core building blocks of a professional manual testing process.

---

## 1. Test Planning 🗺️

A **Test Plan** is the strategic document that outlines the "who, what, when, why, and how" of the entire testing effort. Testing without a plan is just clicking around; professional QA begins with a plan.

* **Analogy:** A test plan is the **battle plan** for an army. You don't just send soldiers (testers) out randomly; you define the objective, the strategy, the resources, and the victory conditions (Exit Criteria) first.

* **Key Components of a Test Plan:**
    * **Scope:** What *will* be tested and what *will not* be tested.
    * **Objectives:** The main goal (e.g., "Verify all new features for the v2.0 release").
    * **Strategy:** The types of testing to be performed (e.g., Functional, Compatibility, Regression).
    * **Resources:** Who is testing? What devices/tools are needed?
    * **Schedule:** Deadlines and milestones for the testing activities.
    * **Entry Criteria:** What must be true to *start* testing? (e.g., "The build is stable and passed Smoke Tests").
    * **Exit Criteria:** What must be true to *finish* testing? (e.g., "100% of critical tests passed, no 'Blocker' bugs open").

---

## 2. Verification and Validation (V&V) ✅

These two terms are the *goal* of all testing, and they are often confused.

* **Verification (Verificación):** "Are we building the product *right*?"
    * This is an *internal* check against the technical requirements and design.
    * **Analogy:** Checking the **blueprints** of a house. Are the walls in the right place? Is the wiring done according to the diagram?
* **Validation (Validación):** "Are we building the *right* product?"
    * This is an *external* check against the user's needs and business goals.
    * **Analogy:** Asking the **homeowner** to live in the house. Is it comfortable? Does it meet their needs? Is the kitchen useful for *them*?

### At a Glance: Verification vs. Validation

| Feature | Verification | Validation |
| :--- | :--- | :--- |
| **Question** | "Are we building the product *right*?" | "Are we building the *right* product?" |
| **Focus** | Process, Design, Specifications | Customer Needs, Business Goals |
| **Timing** | *During* development (e.g., code reviews, checking specs) | *After* a component is built (e.g., UAT, final testing) |

---

## 3. Test Cases and Scenarios 📋

These are the primary tools for documenting manual tests.

* **Test Scenario:** A high-level, "end-to-end" description of a feature to be tested.
    * **Example:** "Verify the user login functionality."
* **Test Case:** A detailed, step-by-step instruction to test a *specific* requirement within that scenario.
    * **Analogy:** A **Test Scenario** is a *recipe title* ("Bake a chocolate cake"). A **Test Case** is the *detailed recipe* (Ingredients, 1. Preheat oven, 2. Mix flour...).
* **Key Components of a Test Case:**
    * **Test Case ID:** A unique identifier (e.g., "TC-LOGIN-001").
    * **Precondition:** What must be true *before* starting (e.g., "User must be on the login page").
    * **Test Steps:** The exact, sequential actions to perform.
    * **Test Data:** The specific input to use (e.g., "User: test@user.com, Pass: P@ssword123").
    * **Expected Result:** What *should* happen after the steps.
    * **Actual Result:** What *did* happen.
    * **Status:** Pass / Fail.

---

## 4. Compatibility Testing 📱💻🖥️

**Compatibility Testing** is a *type* of non-functional test that is critical for manual QA. It verifies that the application looks and works correctly across a wide range of different environments.

* **Analogy:** Checking if your streaming service (the "show") looks and works correctly on all the different "TVs" (Chrome, Safari, a big monitor, a small phone, an iPad).
* **Common Compatibility Checks:**
    * **Browsers:** Google Chrome, Mozilla Firefox, Apple Safari, Microsoft Edge.
    * **Operating Systems:** Windows, macOS, Linux, Android, iOS.
    * **Devices:** Mobile phones (e.g., iPhone 15, Samsung Galaxy), tablets, desktops.
    * **Screen Resolutions:** Testing how the app's layout (UI) adapts to different screen sizes.

 ---
 
## 🚀 Applied Practice: Swag Labs Project

Theory is important, but practice is critical. I have applied all these concepts in a real-world simulation project.

I performed a full manual testing cycle on the **Swag Labs (SauceDemo)** e-commerce website, including:
1.  Creating a **Test Plan**.
2.  Designing a **Test Cases Suite**.
3.  Executing tests and reporting **Bugs** (Jira style).

👉 **[View the Full Manual Testing Project Here](https://github.com/christianviuche/saucedemo-qa-project)**
