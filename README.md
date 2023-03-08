# Argocd-autopilot
This is customised repo for installing Argocd plus a bunch of other Argo project components into
one namespace. The installation process will also apply a number of "out-of-the-box" customisations
to the vanilla install that generally improves the Argo experience.

This can be used with Autopilot as a "from" repo, but you will need to fork it and modify the repo references
to allow it to be used properly.

You do not have write permission to this repo

To install an Argo installation from this autopilot repo, you will need to do the following

* Install `argocd-autopilot` and `argocd` (using `brew` or similar package manager)
* Install `kubectl` and set your context to a Kubernetes installation you have admin permission to
* Fork the `https://github.com/tpayne/argocd-autopilot.git` repo to your own
* Modify the contents of the YAML files to change any GitHub repo mentions to your own repo
* Run the following commands to crearte the Argo deployment. Also, please refer to the Argo-autopilot document below to help define your PAT and other pre-requisites not covered in this spec.

Note - Argo is a constantly developing product, so you may need to review this auto-pilot configuration
to ensure it complies with the latest version you might want to use.

```console
    export GIT_TOKEN=<yourPATToken>
    export GIT_REPO=<yourForkedRepo>
    argocd-autopilot repo bootstrap --recover
```

That will then install a pre-configured Argo suite into your K8s system

# Notes
The following references should also be reviewd: -
- https://argocd-autopilot.readthedocs.io/en/stable/
- https://argocd-autopilot.readthedocs.io/en/stable/#architecture
- https://github.com/argoproj-labs/argocd-autopilot

