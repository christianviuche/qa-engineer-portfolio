# 08: Testing Methodologies & Analysis

This section covers advanced methodologies that define *how* tests are designed and *how* they drive the development process. These are not just "types" of testing, but complete philosophies.

This section also includes **Root Cause Analysis (RCA)**, a critical thinking process for analyzing defects *after* they are found.

---

## 1. Development-Driving Methodologies

These methodologies use tests to *drive* the coding process.

### TDD (Test-Driven Development) ⚙️
**TDD** is a developer-focused methodology where tests are written *before* the code. It follows a very short, repetitive cycle.

* **The Cycle (Red-Green-Refactor):**
    * **Red:** The developer writes a small **Unit Test** for a new feature. The test fails (turns "Red") because the code doesn't exist yet.
    * **Green:** The developer writes the *absolute minimum* amount of code necessary to make that specific test pass (turn "Green").
    * **Refactor:** The developer "cleans up" the code, improving its structure without changing its behavior.
* **Focus:** Code quality, design, and internal structure. It answers the question: "Are we building the code *right*?"

### BDD (Behavior-Driven Development) 🤝
**BDD** is a methodology that evolved from TDD. It focuses on collaboration between developers, QA, and non-technical business people (like the Product Owner).

It uses a simple, human-readable language called **Gherkin** to write "scenarios" that describe the *behavior* of a feature.

* **Gherkin Syntax (Given-When-Then):**
    * `Given` (Dado): A certain context or precondition (e.g., "Given I am on the login page").
    * `When` (Cuando): An action is performed (e.g., "When I enter valid credentials").
    * `Then` (Entonces): The expected outcome (e.g., "Then I should be taken to the dashboard").
* **Focus:** Collaboration and business requirements. It answers the question: "Are we building the *right product*?"

### ATDD (Acceptance Test-Driven Development) ✅
**ATDD** is very similar to BDD. It is a collaborative methodology focused on defining "Acceptance Criteria" *before* development begins. These criteria (acceptance tests) are written from the user's perspective.

* **The Relationship:** BDD, ATDD, and TDD work together.
    * **BDD/ATDD** are used at the "high level" to define what the feature should do (Acceptance Tests).
    * **TDD** is used at the "low level" by the developer to implement that feature (Unit Tests).

---

## 2. Post-Defect Analysis

### RCA (Root Cause Analysis) 🔍
**RCA** is a formal problem-solving process used *after* a critical bug or failure has occurred. The goal is not just to fix the bug, but to understand the *true underlying cause* (the "root cause") to prevent it from ever happening again.

* **Analogy:** A "bug fix" is like taking a painkiller for a headache. An **RCA** is like going to the doctor to find out *why* you are getting headaches (e.g., stress, eye strain, diet) and fixing *that* problem.
* **The "5 Whys" Technique:** A simple and powerful RCA method.
    * **Problem:** The website crashed. (*Why?*)
    * **...Because** the database failed. (*Why?*)
    * **...Because** the database ran out of disk space. (*Why?*)
    * **...Because** the log files were not being deleted. (*Why?*)
    * **...Because** the cleanup job was never scheduled. (**This is the root cause.**)

---

## At a Glance: TDD vs. BDD vs. ATDD

| Feature | TDD (Test-Driven Development) | BDD (Behavior-Driven Development) |
| :--- | :--- | :--- |
| **Perspective** | Developer-centric (Internal) | Team-centric (External Behavior) |
| **Focus** | Code Quality & Design | Collaboration & Business Requirements |
| **Answers...** | "Are we building the code *right*?" | "Are we building the *right thing*?" |
| **Written In** | Code (e.g., JUnit, PyTest) | Plain English (Gherkin: Given/When/Then) |
