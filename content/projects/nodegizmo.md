+++
author = "Kavin"
title = "Nodegizmo"
date = "2023-12-01"
description = "A CLI utility for your Kubernetes nodes"
categories = [
    "kubernetes",
    "golang"
]
+++

A small command-line utility for your Kubernetes nodes.

## Installation
nodegizmo kubectl plugin is available in [krew](https://krew.sigs.k8s.io/) plugin manager. Anyone can install with the following steps:
1. Install `krew` for kuebctl using the following [doc](https://krew.sigs.k8s.io/docs/user-guide/setup/install/).
2. ```bash
    > kubectl krew install nodegizmo
    ```

## Features 🚀
### nodegizmo node
This command displays the generic node related information. For example:
  - NodeName
  - K8sVersion
  - Image
  - OS & Architecture info
  - NodeStatus (Ready/NotReady)
  - Taints
  - Node Provider (AWS/Azure/GCP)
  - Topology info (Region & Zone)
{{< figure src="/images/nodegizmo-node.png"  class="center" width="1000" height="500" >}}

### nodegizmo node capacity
Node Capacity information
  - CPU
  - Memory
  - Disk
  - Ephemeral storage
  - Pod capacities
- Nodepool related information
{{< figure src="/images/nodegizmo-node-cp.png"  class="center" width="1000" height="500" >}}

### nodegizmo nodepool
Nodepool related information
  - Grouped by NodePool ID
  - Node list
  - Topology info (Region & Zone)
  - Instance type
  - K8sVersion
  - Nodepool provider (supported: EKS/AKS/GKE/Karpenter)
{{< figure src="/images/nodegizmo-nodepool.png"  class="center" width="1000" height="500" >}}

### nodegizmo exec nodeName
Exec into any node by spawning a `nsenter` pod automatically based on the node selection.