# Argocd-autopilot

## Overview
This repository is designed to simplify the installation of Argo CD along with various Argo project components into a single Kubernetes namespace. The aim is to provide enhanced configurations and best practices for seamless deployments.

## Key Improvements
1. **In-Depth Examples:** This repository includes examples for common use cases to facilitate a quicker onboarding process.
2. **Centralized Configuration Management:** Sensitive information is stored in `config.yaml` to streamline the management of tokens and URLs.
3. **Automated Testing and CI/CD:** Integration of GitHub Actions for automated testing of configurations.
4. **RBAC and Security Improvements:** Detailed documentation on configuring RBAC policies according to the principle of least privilege.
5. **User Feedback Section:** Encouragement for users to provide feedback or report issues through GitHub.

## Setup Instructions
### Install Argo CD and Required Tools
1. Install `argocd-autopilot` and `argocd` using a package manager.
2. Install `kubectl` and set up your Kubernetes context appropriately.
3. Fork the repository and modify it as necessary.
4. Run the following commands:

   ```bash
   export GIT_TOKEN=<yourPATToken>
   export GIT_REPO=<yourForkedRepo>
   argocd-autopilot repo bootstrap --recover
   ```

### Example Application Deployment
To deploy an application using ArgoCD Autopilot, run:
```bash
argocd-autopilot app create myapp --app <app-specifier> -p <project-name>
```

## Configuration Management
The `config.yaml` file is utilized to store sensitive configurations. Here’s an example:
```yaml
argocd_token: <your_token>
argocd_repo_url: https://github.com/tpayne/argocd-autopilot.git
```