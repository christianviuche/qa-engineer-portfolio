
# 16: Version Control Systems (VCS)

In the world of automation and DevOps, **Test Code is Production Code.**

This means QA Engineers must manage their automation scripts just like developers manage their application code: tracking changes, collaborating on features, and maintaining a history of everything. This is what a **Version Control System (VCS)** does.

---

## 1. The System: Git <img src="https://cdn.simpleicons.org/git/8C00FF" alt="Git logo" width="20" height="20" valign="middle">

**Git** is the specific software tool (the "engine") that runs locally on your computer. It tracks every modification to every file in your project.

* **Analogy:** Git is like the "Save" feature in a video game, but on steroids. It lets you create "save points" (Commits), go back in time if you make a mistake (Revert), and try out new strategies in a parallel timeline (Branches).
* **Key Concepts for QA:**
    * **Repository (Repo):** The folder containing your project and its history.
    * **Commit:** A snapshot of your changes at a specific moment.
    * **Branch:** A parallel version of the code (e.g., `feature/login-test`).
    * **Merge:** Combining changes from one branch into another.

---

## 2. Repo Hosting Services ☁️

While Git works on your computer, **Hosting Services** are where you store that code in the cloud to share it with your team. They add a social and management layer on top of Git.

### GitHub <img src="https://cdn.simpleicons.org/github/8C00FF" alt="GitHub logo" width="20" height="20" valign="middle">
* **Overview:** The most popular code hosting platform in the world (owned by Microsoft).
* **Why it matters:** It is the home of Open Source. Most automation frameworks and libraries live here. It introduced the concept of the **"Pull Request" (PR)**, which is how teams review code before merging it.
* **QA Context:** This portfolio is hosted on GitHub!

### GitLab <img src="https://cdn.simpleicons.org/gitlab/8C00FF" alt="GitLab logo" width="20" height="20" valign="middle">
* **Overview:** A complete DevOps platform delivered as a single application.
* **Why it matters:** GitLab is famous for its built-in **CI/CD pipelines**. It is widely used in enterprise environments where the code repository and the pipeline (Jenkins replacement) are in the same tool.
* **QA Context:** You will often define your automated test runs inside a `.gitlab-ci.yml` file.

### Bitbucket <img src="https://cdn.simpleicons.org/bitbucket/8C00FF" alt="Bitbucket logo" width="20" height="20" valign="middle">
* **Overview:** The hosting service owned by **Atlassian**.
* **Why it matters:** Its superpower is **Jira integration**. Since they are from the same company, linking a code change (Commit) to a user story (Jira Ticket) is seamless.
* **QA Context:** If your company uses Jira heavily, they likely use Bitbucket for code.
