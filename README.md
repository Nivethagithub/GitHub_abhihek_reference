# GitHub-Actions-Zero-to-Hero
Repository to kick start your journey with GitHub Actions

## Comparing with Jenkins 

### Advantages of GitHub Actions over Jenkins

- Hosting: Jenkins is self-hosted, meaning it requires its own server to run, while GitHub Actions is hosted by GitHub and runs directly in your GitHub repository.

- User interface: Jenkins has a complex and sophisticated user interface, while GitHub Actions has a more streamlined and user-friendly interface that is better suited for simple to moderate automation tasks.

- Cost: Jenkins can be expensive to run and maintain, especially for organizations with large and complex automation needs. GitHub Actions, on the other hand, is free for open-source projects and has a tiered pricing model for private repositories, making it more accessible to smaller organizations and individual developers.

### Advantages of Jenkins over GitHub Actions

- Integration: Jenkins can integrate with a wide range of tools and services, but GitHub Actions is tightly integrated with the GitHub platform, making it easier to automate tasks related to your GitHub workflow.

In conclusion, Jenkins is better suited for complex and large-scale automation tasks, while GitHub Actions is a more cost-effective and user-friendly solution for simple to moderate automation needs.

### When to use Github 
  - If your project is small and for demo purpose.
  - If you don't want to migrate for project for any other CICD tools (Azure DevOps, GitLab, Jenkins).
  - If you don't have the self hosted runner, github offer runs and has some limitations of the runtime of CICD jobs.

### concise summary of the runtime limitations for CI/CD jobs in GitHub Actions:

* Job Execution: Max 6 hours on GitHub-hosted runners (configurable, but practically limited on self-hosted too).
Workflow Run: Max 35 days total.
Self-Hosted Queue: Jobs queued for self-hosted runners are canceled after 24-48 hours.
API Requests: Max 1,000 per hour per repository.
Webhook Events: Max 1500 triggering events per 10 seconds per repository.
Concurrent Jobs: Limited by your GitHub plan.
Job Matrix: Max 256 jobs per workflow run.
Workflow Run Queue: Max 500 queued per 10 seconds per repository.
