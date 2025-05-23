# README for Argocd-autopilot

## Argocd-autopilot
This repository is designed for installing ArgoCD and additional components into a single namespace with enhanced configurations.

### Improvements
This project has undergone several improvements including:

1. **In-Depth Examples:** Each application type now includes examples for faster onboarding.
2. **Centralized Configuration:** Sensitive configurations such as Git tokens and repository URLs are maintained in a separate `config.yaml` for ease of management.
3. **User Feedback Mechanism:** Users are encouraged to engage via GitHub issues for feedback and improvement suggestions.
4. **Security Enhancements:** RBAC settings have been reviewed and tightened to follow the principle of least privilege.
5. **Automated Testing:** The repository integrates automated validation tests to ensure configurations are correct and perform as expected.
6. **Performance Monitoring:** Prometheus metrics can be integrated to monitor application performance and health.

### Setup Instructions
#### Initial Setup
To establish an installation of ArgoCD from this autopilot repository, follow these steps:

1. Install `argocd-autopilot` and `argocd` (via `brew` or another package manager).
2. Install `kubectl` and configure your context to a Kubernetes installation with admin permissions.
3. Fork this repository to your own GitHub account.
4. Modify YAML files to update any repository references to your own.
5. Run the commands:

   ```shell
   export GIT_TOKEN=<yourPATToken>
   export GIT_REPO=<yourForkedRepo>
   argocd-autopilot repo bootstrap --recover
   ```

This will install a pre-configured ArgoCD suite into your Kubernetes cluster.

### Important Notes
Review the included references for detailed documentation and updates:
- [ArgoCD Autopilot Documentation](https://argocd-autopilot.readthedocs.io/en/stable/)
- [GitHub Repo for ArgoCD Autopilot](https://github.com/argoproj-labs/argocd-autopilot) 

*This repository is actively developed; ensure to periodically check for updates.*