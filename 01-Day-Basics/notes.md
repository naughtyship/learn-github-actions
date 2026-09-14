

## What is GitHub Actions?

GitHub Actions is a CI/CD and automation platform provided by GitHub. It lets you automatically run tasks in response to repository events (push, pull request, release, schedule, etc.).

Example workflow (high level):

1. Developer pushes code to the repository
2. A workflow run starts: build → test → security scan → create artifact

## Why use GitHub Actions?

- **Save time:** Automate builds, tests, packaging, and deployments.
- **Reduce errors:** Consistent repeatable processes reduce human mistakes.
- **Deep GitHub integration:** Workflows can react to pull requests, issues, releases, and other GitHub events.

## Alternatives

- Azure DevOps Pipelines
- GitLab CI/CD
- Jenkins
- Others (Argo CD — focused on Kubernetes GitOps, not a full CI replacement)

## Git / GitHub / GitHub Actions / GitLab — quick distinctions

- **Git:** Distributed version control system that tracks code changes.
- **GitHub:** Hosting and collaboration platform for Git repositories.
- **GitHub Actions:** Automation (CI/CD) platform built into GitHub.
- **GitLab:** DevOps platform that includes Git hosting and CI/CD features.

## GitHub Actions terminology mapping with Azure Devops

| Azure DevOps term | GitHub Actions equivalent |
|---|---|
| Pipeline | Workflow |
| Pipeline trigger | Event |
| Stage | Job |
| Task | Step / Action |
| Agent | Runner |
| Agent Pool | Runner group |
| Pipeline variable | Variable |
| Secret variable | Secret |
| Variable Group | Variables / Secrets / Environment configuration |
| Pipeline parameter | Workflow input |
| dependsOn | needs |
| condition | if |
| Pipeline artifact | Artifact |
| Environment | Environment |
| YAML template | Reusable workflow / Composite action |
| Service connection | Credentials / OIDC / authentication configuration |
| Azure Repos | GitHub repository |
| Pull Request | Pull Request |
| Build | Workflow run |
| Pipeline run | Workflow run |

## Notes

- Use descriptive workflow names and small focused jobs for readability.
- Keep secrets in GitHub Secrets or use OIDC for cloud auth.
- Reuse common steps via composite actions or reusable workflows.
