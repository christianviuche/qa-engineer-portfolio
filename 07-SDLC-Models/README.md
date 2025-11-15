# 07: SDLC Delivery Models

The **Software Development Life Cycle (SDLC)** is a conceptual framework that defines the complete process for creating, deploying, and maintaining software.

The chosen SDLC model is a project's most critical decision, as it defines how teams communicate, how change is handled, and—most importantly for us—**where, when, and how QA is involved.**

---

## 1. Traditional (Sequential) Models ➡️

These models are linear and rigid. Each phase must be 100% complete before the next one can begin. Change is seen as a problem and is expensive.

### Waterfall 🌊
The project flows in one direction.

#### Waterfall Phases:
1.  **Requirements:** *All* project scope is defined and documented. Once approved, this document is "frozen."
2.  **Design:** Architects design the entire system architecture based on the requirements.
3.  **Implementation (Coding):** Developers write *all* of the product's code.
4.  **Testing (Verification):** The *entire, complete* product is delivered to the QA team.
5.  **Deployment:** The final product is installed and delivered to the client.
6.  **Maintenance:** Bugs are fixed and minor improvements are added.

* **Role of QA in Waterfall:** QA is an **isolated, final phase**. The QA team acts as a "gatekeeper" at the end of the process.
* **Pros:** Very structured, documented, and easy to manage *if* requirements are 100% clear and will never change.
* **Cons:** Extremely rigid. If a design flaw is found in the Testing phase, it is catastrophic and expensive to fix. Bugs are found very late.

### V-Model ✅
An evolution of Waterfall that attempts to improve QA's role by linking every development phase to a corresponding testing phase.

#### The "V": Verification (Left) vs. Validation (Right)
The V-Model shows that testing (Validation) should be planned *at the same time* as development (Verification).

* **Business Requirements** <-> **Acceptance Testing (UAT):** Did we build the product the client *wanted*?
* **System Design** <-> **System Testing:** Does the *complete* system (functional & non-functional) work as designed?
* **Architecture Design** <-> **Integration Testing:** Do the *modules* of the system interact correctly?
* **Module Design** <-> **Unit Testing:** Does the *code* for each individual function work?
* **Coding:** This is the bottom point of the "V."

* **Role of QA in V-Model:** QA gets involved *much earlier* in the planning process to write the UAT, System, and Integration test plans. However, the *execution* of these major tests still happens late in the cycle.

---

## 2. Agile Models (Iterative) 🔄

**Agile** is not a "model" like Waterfall; it is a **philosophy** or *mindset* for developing software, based on the values of the [Agile Manifesto](https://agilemanifesto.org/).

The core idea is to stop building "one big product" over a year. Instead, you build and deliver **small, functional pieces** (increments) in very short cycles (iterations).

### QA's Role in Agile: "Shift-Left Testing"
This is the most critical change. In Agile:
* QA is **NOT** a phase at the end.
* QA is an **integrated member of the development team**.
* The goal of QA is not to "find bugs" but to **"prevent bugs."**
* This is called **"Shift-Left"**: moving QA activities (testing, requirements review) as far to the *left* (the beginning) of the process as possible.

---

## Agile Frameworks (The "How-To")

If Agile is the philosophy, these are the *frameworks* for implementing it.

### Scrum 🏉
The most popular Agile framework. Work is divided into fixed-time cycles called **"Sprints"** (usually 2-4 weeks).

* **Key Roles:**
    * **Product Owner (PO):** Defines the "what" (the requirements, or "User Stories").
    * **Scrum Master:** Facilitates the Scrum process and removes impediments.
    * **Development Team:** The self-organizing team that builds the product. **QA is part of this team.**
* **Key Events (Ceremonies):**
    * **Sprint Planning:** The team plans the work they can complete in the next Sprint.
    * **Daily Scrum:** A 15-min daily meeting (What did I do yesterday? What will I do today? What impediments do I have?).
    * **Sprint Review:** The team *demonstrates* the working software they completed ("Demo").
    * **Sprint Retrospective:** The team reflects on *how* they worked to improve their process.
* **Analogy:** Like planning a series of short, 2-week *sprints* in a race. The goal is to finish a segment, review, and plan the next one.

### Kanban 📋
An Agile framework focused on **visualizing workflow** and continuous flow. It does not use "Sprints."

* **Key Concepts:**
    * **Visualize the Workflow:** Using a **Kanban Board** (like Trello or Jira) with columns (e.g., "To Do," "In Progress," "Ready for QA," "Done").
    * **Limit "Work In Progress" (WIP):** The core of Kanban. A limit is set on how many tasks can be in one column (e.g., "Ready for QA" can only have 3 tasks). This prevents bottlenecks and forces collaboration.
    * **Manage Flow:** The goal is to move tasks from left to right as smoothly and quickly as possible.
* **Analogy:** A restaurant kitchen. A new order (task) goes on the board, moves through 'Cooking' (In Progress), and then to 'Service' (Done). The goal is a smooth, continuous flow.

### XP (Extreme Programming) 💻
A framework highly focused on technical excellence and code quality.

* **Key Practices:**
    * **Test-Driven Development (TDD):** Developers must write the (failing) unit test *before* they write the code to make it pass.
    * **Pair Programming:** Two developers work at one computer.
    * **Continuous Integration (CI):** Code is integrated and tested automatically many times per day.

### SAFe (Scaled Agile Framework) 🏢
A very complex framework for applying Agile and Scrum to **massive, enterprise-level** organizations (hundreds or thousands of developers).

* **Key Concept:** It's an "operating system" for large Agile companies. It adds layers of planning (like the "Agile Release Train" and "PI Planning") to coordinate all the teams.

---

## At a Glance: Waterfall vs. Agile ⚖️

| Feature | Waterfall (Traditional) | Agile (Modern) |
| :--- | :--- | :--- |
| **Philosophy** | Linear / Sequential | Iterative / Incremental |
| **Flexibility** | **Rigid.** Change is a problem. | **Flexible.** Change is welcomed. |
| **Testing** | A separate phase at the **end** of the project. | A **continuous** activity during the entire project. |
| **Role of QA** | **"Gatekeeper"** (Finds bugs at the end) | **"Collaborator"** (Prevents bugs from the start) |
| **Delivery** | One large product delivered at the end. | Small, functional pieces delivered every few weeks. |
| **Best For...** | Projects with 100% fixed, unchanging requirements (e.g., building a bridge). | Projects where requirements evolve or are not fully known (most software). |
