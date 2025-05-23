# Projects Documentation
This directory contains all your `argocd-autopilot` projects defined for logical grouping of applications.

### Creating a New Project
To create a new project, execute:

```bash
export GIT_TOKEN=<YOUR_TOKEN>
export GIT_REPO=<REPO_URL>

argocd-autopilot project create <PROJECT_NAME>
```

### Creating Projects for Different Clusters
If you wish to create a project that deploys applications to a different cluster, run:

```bash
export GIT_TOKEN=<YOUR_TOKEN>
export GIT_REPO=<REPO_URL>

argocd-autopilot project create <PROJECT_NAME> --dest-kube-context <CONTEXT_NAME>
```

#### RBAC Considerations
- Regularly review permission policies to ensure the principle of least privilege is adhered to, especially in shared environments.

### Notes
Review the [Argocd-autopilot documentation](https://argocd-autopilot.readthedocs.io/en/stable/) for more detailed instructions.