# Wordsmith Kubernetes Manifests (Kustomize)

Wordsmith is the demo project originally from [dockersamples/wordsmith](https://github.com/dockersamples/wordsmith)

The demo app runs across three containers:

- **[api](https://github.com/bretfisher/wordsmith-api)** - a Java REST API which serves words read from the database
- **[web](https://github.com/bretfisher/wordsmith-web)** - a Go web application that calls the API and builds words into sentences
- **db** - a Postgres database that stores words

## Kubernetes Kustomize Manifests

The three pods/containers of this app are in the `./manifests` directory and those files rarely change. They are plain Kubernetes manifests.

For each environment, we create a directory in `./environments` and add a `kustomization.yaml` file, which is a [Kustomize](https://kustomize.io/) manifest that pulls in the base manifests and adds environment-specific changes.