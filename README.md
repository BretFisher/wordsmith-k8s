# Wordsmith Kubernetes Manifests (Kustomize)

Wordsmith is the demo project originally from [dockersamples/wordsmith](https://github.com/dockersamples/wordsmith)

The demo app runs across three containers:

- **[api](https://github.com/bretfisher/wordsmith-api)** - a Java REST API which serves words read from the database
- **[web](https://github.com/bretfisher/wordsmith-web)** - a Go web application that calls the API and builds words into sentences
- **db** - a Postgres database that stores words

## Kubernetes Kustomize Manifests

The three pods/containers of this app are in the `./manifests` directory.


## Architecture

![Architecture diagram](architecture.excalidraw.png)
