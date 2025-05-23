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
- Set appropriate roles for users in your AKS cluster to ensure a secure deployment process.
- Use least privilege access strategies to define user permissions.

### Example Project YAML
Here’s an example of a project configuration in YAML format:
```yaml
apiVersion: argoproj.io/v1alpha1
kind: AppProject
metadata:
  name: myproject
  namespace: argocd
spec:
  description: My Project for ArgoCD
  destinations:
    - server: https://kubernetes.default.svc
      namespace: argocd
  sourceRepos:
    - '*'
```