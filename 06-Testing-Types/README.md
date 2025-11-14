
# 06: The Catalog of Testing Types

This section covers the main catalog of software testing types. Every test falls into one of two major categories: **Functional** (verifying *what it does*) or **Non-Functional** (verifying *how well it does it*).

---

## At a Glance: Functional vs. Non-Functional

| Feature | Functional Testing ⚙️ | Non-Functional Testing ⚡ |
| :--- | :--- | :--- |
| **Verifies...** | **What** the system does (Features) | **How** the system works (Quality) |
| **Based on...** | Business Requirements / User Stories | Quality Attributes / SLA |
| **Objective** | Validate functions | Validate performance & usability |
| **Example** | "Does the login button work?" | "Can 1000 users log in at the same time?" |

---

## 1. Functional Testing Types

These tests verify the *features* and *functions* of the software.

### Unit Testing 
* **What:** Testing the smallest, most isolated piece of code possible (a single function or method).
* **Who:** Almost always done by the Developer.
* **Analogy:** Testing a single "brick" to see if it's solid.

### Integration Testing 
* **What:** Testing how two or more "units" (components or modules) work *together*.
* **Who:** Developers and specialized QAs (SDETs).
* **Analogy:** Testing if the "bricks" and "mortar" (la mezcla) stick together correctly.

### Smoke Testing 
* **What:** A quick, superficial set of tests to ensure the *most critical functions* of a new build are working. If a smoke test fails, the build is rejected immediately.
* **Who:** QA and sometimes automated (CI/CD).
* **Analogy:** A plumber installing pipes. Before leaving, they open the main valve for 1 minute to check for *major leaks* (smoke). They aren't testing every single faucet.

### Sanity Testing 
* **What:** A very specific, narrow set of tests performed *after a small bug fix or change* to ensure the fix works and hasn't broken the *immediate* surrounding area.
* **Who:** QA.
* **Analogy:** A mechanic changes a tire. A sanity test is starting the car to make sure the "low tire pressure" light went off. It's not a full test drive (that's regression).

### Regression Testing 
* **What:** A broad set of tests designed to ensure that *new code changes* have not *broken existing features* (i.e., caused a "regression").
* **Who:** QA (often automated).
* **Analogy:** A mechanic changes the oil. A regression test is a full test drive to make sure the brakes, radio, windows, and headlights *still work* (even though they weren't touched).

### Exploratory Testing 
* **What:** Testing without a script. The tester uses their creativity, curiosity ("QA Mindset"), and experience to "explore" the application and find bugs that scripts would miss.
* **Who:** QA.
* **Analogy:** Exploring a new city *without a map*. You are actively looking for interesting (or problematic) areas based on your intuition.

### UAT 
* **What:** The *final* stage of testing where the *client* or *end-users* test the software to confirm it meets their business requirements and they "accept" it.
* **Who:** The Client / Stakeholders / End-Users.
* **Analogy:** The customer (you) doing a final test drive of a car *before* you buy it.

### Mocking 
* **Note:** This is a *technique*, not a *type*, but it's essential for testing.
* **What:** Creating a "mock" or "fake" version of a component that your code depends on. For example, creating a fake database or a fake API.
* **Why:** It lets you run a **Unit Test** in isolation without needing a real database or a live API connection.

---

## 2. Non-Functional Testing Types

These tests verify the *quality attributes* (performance, security, etc.) of the system.

### Performance Testing 
* **What:** The *umbrella term* for testing speed, stability, and scalability. Load and Stress testing are *types* of Performance Testing.
* **Who:** Specialized QA / Performance Engineers.
* **Analogy:** Testing a car's overall performance (top speed, acceleration, handling).

### Load Testing 
* **What:** Testing how the system behaves under a *specific, expected load* (e.g., 500 concurrent users).
* **Goal:** To find bottlenecks and ensure the system is stable under normal conditions.
* **Analogy:** Checking if the car drives well with a *normal* load (4 people inside).

### Stress Testing 
* **What:** Testing how the system behaves *beyond* its normal limits, often until it *breaks*.
* **Goal:** To find the system's "breaking point" and check if it recovers gracefully.
* **Analogy:** Checking how the car handles an *abnormal* load (8 people + luggage on the roof) until the suspension breaks.

### Security Testing 
* **What:** Testing to find vulnerabilities and ensure the system is secure from attacks (like SQL Injection, XSS, etc.).
* **Who:** Specialized Security Testers (Ethical Hackers).
* **Analogy:** Checking if a car's locks, alarm, and ignition system can be bypassed by a thief.

### Accessibility Testing 
* **What:** Testing to ensure the application is usable by people with disabilities (e.g., color blindness, vision impairment, motor disabilities).
* **Focus:** Screen reader compatibility, keyboard-only navigation, color contrast.
* **Analogy:** Checking if a car is designed to be usable by someone in a wheelchair or with other physical limitations.
