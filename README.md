# Wordsmith Kubernetes Manifests (Kustomize)

Wordsmith is the demo project originally from [dockersamples/wordsmith](https://github.com/dockersamples/wordsmith)

## Kubernetes Kustomize Manifests

The pods/containers of this app are in the `./base` directory and those files rarely change. They are plain Kubernetes manifests.

For each environment, we create a directory in `./environments` and add a `kustomization.yaml` file, which is a [Kustomize](https://kustomize.io/) manifest that pulls in the base manifests and overrides environment-specific values.

These environment overrides can be consumed by Argo CD, Flux, or applied by kubectl directly with `kubectl apply -k environments/<env>`. 