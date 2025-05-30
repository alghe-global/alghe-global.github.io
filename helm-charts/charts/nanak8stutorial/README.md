# Helm Chart for YouTube K8s project tutorial by Nana

## Introduction

Nana has put out a [tutorial on YouTube on Nov 6, 2020](https://www.youtube.com/watch?v=X48VuDVv0do) regarding Kubernetes for beginners.

In this tutorial one is walked through creating resources with Kubernetes such as deployments, services, ingress, volumes and StatefulSets.

> WARNING: This chart is provided as a bare bones chart. Secrets in `values.yaml` are in plaintext. DO NOT STORE secrets used in production (whatever stage) in this file. Doing so is at YOUR OWN RISK, especially if committing to a public repo.

## Prerequisites

This chart was used on a Debian 12 machine with kernel 6.1.0-33-amd64, minikube version v1.35.0 and docker 28.1.0. What else is needed:

* Kubernetes v1.32.0
* Helm v3.17.2
* Ingress addon enabled for minikube
* Dashboard initialized with minikube
* Host machine's /etc/hosts populated for `dashboard.com` entry

## Get Repository Info

```console
helm repo add alghe-global https://alghe-global.github.io/helm-charts
helm repo update
```

## Installing Chart

```console
helm install [RELEASE_NAME] alghe-global/NanaK8sTutorial
```

## Upgrading Chart

```console
helm upgrade [RELEASE_NAME] [CHART] --install
```

## Uninstall Chart

```console
helm uninstall [RELEASE_NAME]
```

## License

[Apache 2.0 License](https://github.com/alghe-global/alghe-global.github.io/blob/master/helm-charts/LICENSE)
