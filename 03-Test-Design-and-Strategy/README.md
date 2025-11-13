# 03: Test Design and Strategy

This section covers two critical concepts that elevate simple test execution to a professional, efficient QA process:

1.  **Test Oracles:** Knowing *how to determine* if a test passed or failed.
2.  **Test Prioritization:** Knowing *which test to run first* when time is limited.

---

## Concept Definitions

### 1. Test Oracle (Oráculo de Prueba)

A Test Oracle is **not** a person. It is the **mechanism, source of truth, or principle** used to determine whether the outcome of a test is correct.

It is the "answer key" against which you compare the software's behavior. A test is useless if you don't have a reliable way to know if the result is right or wrong.

* **Analogy:** If testing is a math exam, the **Test Oracle** is the **teacher's answer sheet** you use to grade it.
* **Goal:** To provide a definitive Pass/Fail verdict for a test.
* **Orientation:** Verification ✅/❌
* **Answers:** "How do I know this is the *correct* output?"
* **Common Types of Oracles:**
    * **Specification/Documentation:** The requirements, user story, or design spec. (e.g., "The spec says this button must be blue.")
    * **Heuristic Oracles:** Using "rules of thumb" or common sense. (e.g., "A 404 error is not an acceptable result for a search.")
    * **Consistency Oracles:** Comparing the result to a previous version (Regression Testing) or a similar component. (e.g., "It should look the same as it did yesterday.")
    * **Algorithmic Oracles:** Using a separate program or calculation (like a calculator) to determine the correct result.

### 2. Test Prioritization (Priorización de Pruebas)

Test Prioritization is the strategic process of deciding **which tests to run and in what order**. In the real world, you rarely have time to run *all* tests, so you must run the *most important* ones first.

This is a risk-management activity designed to find the most critical bugs as quickly as possible.

* **Analogy:** A doctor in an **Emergency Room**. They don't treat patients in the order they arrive; they treat the most **critical** patients first (triage). That is prioritization.
* **Goal:** To maximize risk coverage, find critical defects early, and use limited testing time efficiently.
* **Orientation:** Risk Management & Efficiency ⏳
* **Answers:** "Given I only have 1 hour, what tests *must* I run to protect the business?"
* **Common Prioritization Criteria:**
    * **Risk-Based:** What features, if broken, would be catastrophic? (e.g., "Login" or "Payment Checkout" are high priority).
    * **Frequency of Use:** What features are used most by customers?
    * **Recent Code Changes:** Test areas where the code was just modified (high chance of new bugs).
    * **Bug History:** Test areas that have historically been buggy.

---

## At a Glance: Oracle vs. Prioritization

| Feature | Test Oracle | Test Prioritization |
| :--- | :--- | :--- |
| **Main Question** | "How do I know if this test passed or failed?" | "Which test should I run first?" |
| **Focus** | Accuracy & Verification (Correctness) | Risk, Value, & Efficiency (Time) |
| **Goal** | To determine the Pass/Fail verdict | To maximize bug-finding efficiency |
| **Analogy** | The Answer Key | The ER Triage Nurse |
