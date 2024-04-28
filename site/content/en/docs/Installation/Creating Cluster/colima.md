---
title: "Colima"
linkTitle: "Colima"
weight: 100
description: >
  Follow these steps to create a Colima Kubernetes cluster
  for your Agones install.
---

## Installing Colima

First, [install Colima](https://github.com/abiosoft/colima/blob/main/docs/INSTALL.md) through one of the proposed installation methods.

## Starting Colima

Colima by itself is just a container runtime, but through flags kubernetes (in this case [k3s](https://k3s.io/))can be installed directly inside the container.

```bash
colima start --kubernetes --kubernetes-version v{{% minikube-example-cluster-version %}}
```

{{< alert title="Note" color="info">}}
You may need to increase the `--cpu` or `--memory` values for your colima instance, depending on what resources are
available on the host and/or how many GameServers you wish to run locally.

{{< /alert >}}

## Next Steps

- Continue to [Install Agones]({{< relref "../Install Agones/_index.md" >}}).
