# Documentation for Creating Projects

This section has been enhanced to include best practices and examples for creating new projects.

## Creating a New Project
To create a new project, run:

```bash
export GIT_TOKEN=<YOUR_TOKEN>
export GIT_REPO=<REPO_URL>

argocd-autopilot project create <PROJECT_NAME>
```

## Creating Projects for Different Clusters
```bash
export GIT_TOKEN=<YOUR_TOKEN>
export GIT_REPO=<REPO_URL>

argocd-autopilot project create <PROJECT_NAME> --dest-kube-context <CONTEXT_NAME>
```

- Ensure to review the `RBAC` settings for proper access control.
