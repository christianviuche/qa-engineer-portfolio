
# 17: CI/CD Pipelines 

**CI/CD** is the backbone of modern DevOps and Agile software delivery. For a QA Engineer, this is where our automated tests "live" and run automatically.

* **CI (Continuous Integration):** The practice of merging code changes frequently (e.g., daily). Every merge triggers an *automated pipeline* that builds the app and **runs the tests**. If tests fail, the merge is rejected.
* **CD (Continuous Delivery/Deployment):** If the CI stage passes (all tests green), the code is automatically deployed to a test environment (Delivery) or straight to production (Deployment).

---

## Key Tools & Platforms

### 1. The Industry Standards

* **Jenkins:** <img src="https://cdn.simpleicons.org/jenkins/8C00FF" alt="Jenkins logo" width="20" height="20" valign="middle">
    * **Type:** Open Source / Self-Hosted.
    * **Use:** The "grandfather" of CI tools. It is extremely powerful and flexible thanks to thousands of plugins, but it requires a lot of manual configuration and maintenance. It uses "Jenkinsfiles" (Groovy) to define pipelines.
* **GitLab CI:** <img src="https://cdn.simpleicons.org/gitlab/8C00FF" alt="GitLab logo" width="20" height="20" valign="middle">
    * **Type:** Integrated Platform.
    * **Use:** A favorite in modern DevOps because the CI/CD is built directly into the code repository. You define pipelines using a simple YAML file (`.gitlab-ci.yml`).
* **Azure DevOps:**
    * **Type:** Enterprise Cloud.
    * **Use:** Microsoft's all-in-one solution. It is massive in the enterprise world and integrates tightly with .NET and Azure cloud environments.

### 2. Cloud-Native & SaaS Tools

* **CircleCI:** <img src="https://cdn.simpleicons.org/circleci/8C00FF" alt="CircleCI logo" width="20" height="20" valign="middle">
    * **Use:** Known for its speed and ease of setup with GitHub. It's purely cloud-based and very popular with startups.
* **Travis CI:** <img src="https://cdn.simpleicons.org/travisci/8C00FF" alt="Travis CI logo" width="20" height="20" valign="middle">
    * **Use:** One of the first CI tools to integrate seamlessly with GitHub. It is simple to use for open-source projects.

### 3. Ecosystem-Specific Tools

* **Bamboo:** <img src="https://cdn.simpleicons.org/bamboo/8C00FF" alt="Bamboo logo" width="20" height="20" valign="middle">
    * **Use:** Atlassian's CI tool. Its superpower is deep integration with Jira and Bitbucket. If a test fails in Bamboo, it can automatically create a bug in Jira.
* **TeamCity:** <img src="https://cdn.simpleicons.org/teamcity/8C00FF" alt="TeamCity logo" width="20" height="20" valign="middle">
    * **Use:** Created by JetBrains (makers of IntelliJ/PyCharm). It is known for its incredible developer experience and "smart" features, but it is a paid product.
* **Drone:** <img src="https://cdn.simpleicons.org/drone/8C00FF" alt="Drone logo" width="20" height="20" valign="middle">
    * **Use:** A container-native CI tool. It runs every step of the pipeline inside a Docker container, making it very clean and modern.
