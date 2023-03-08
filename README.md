# argocd-autopilot
This is an initial customised repo for installing Argocd plus a bunch of other Argo project components into
one namespace

This can be used with Autopilot as a "from" repo, but you will need to fork it and modify the repo references
to allow it to be used properly.

You do not have write permission to this repo

To install an Argo installation from this autopilot repo, you will need to do the following

* Install `argocd-autopilot` and `argocd` (using `brew` or similar package manager)
* Install `kubectl` and set your context to a Kubernetes installation you have admin permission to
* Fork the `https://github.com/tpayne/argocd-autopilot.git` repo to your own
* Run the following commands should then spin up 

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

