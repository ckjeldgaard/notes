---
sidebar_position: 2
---

# Kubernetes

Exam tests deployment process

- "Build it"
- Container Registry - "Store it"
- Kubernetes Engine - "Deploy and run it"

## GKE (Google Kubernetes Engine)

- A **cluster** is at least one **control pane** and multiple worker machines, a.k.a. **nodes**.
- **Zonal** and **regional** clusters. Two types of zonal clusters:
  - _Single zone cluster:_ Single control plane running in one zone. This control plane manages workloads on nodes running only in the same node.
  - _Multi zonal cluster:_ Runs in multiple zones. But it has only a single replica of the control pane. If higher availability is needed, it's a better option to go with a regional cluster. 
- Private clusters are VPC-native clusters
- For highly available apps, distribute using multi-zonal node pools.
- **Horizontal Pod Autoscaler (HPA)** checks workload metrics against thresholds
- Use **Workload Identity** to connect clusters to other Google services.

:::tip To change the machine type in a cluster
Create a new node pool in the cluster with the desired machine type and then migrate the workload to the new node pool.
:::

To perform rolling updates:

Execute the command `'kubectl set image deployment/<OLD_DEPLOYMENT> <NEW_DEPLOYMENT>'` 

## Terminology

- **Node:** VM's containers are hosted on
- **Node pool:** Group of nodes
- **Cluster:** One or more node pools
- **Node image:** Node-level OS image
- **Pods:** Smallest deployable unit
- **Container image:** Base image used in container

## Dictionary

- **Deployment:** Stateless applications. _ReadOnlyMany_ or _ReadWriteMany_ volumes.
- **StatefulSets:** Stateful apps. Persistent ID for each pod
- **DaemonSets:** One pod per node (background tasks)
- **ConfigMap:** Env vars, CLI args etc. to containers at run-time
- **ReplicaSet:** Ensures that a specified number of pod replicas are running at any given time.

## Anthos

- Application deployment anywhere: GCP, on-premise, hybrid and multi-cloud (AWS and Azure)
- Kubernetes Engine, Cloud Run and VM's
- **Migrate for Anthos**: Migrate existing apps to GKE
- CI/CD automated pipelines

### Anthos Service Mesh

- Manage microservices. Communication of services on-premise and GCP
- Powered by **Istio**
- Controls traffic flow.
  - Support canary and blue-green deployments.
  - Load balancing
  - Monitoring, logging and trace
- Can simulate fault injections like:
  - **Network latency**
  - **HTTP error codes**

### Anthos GKE connection

- Extending GKE to work in multiple environments
- **Anthos on GCP** uses "traditional" GKE, while **on-premises** uses **VMWare** and **Bare Metal**.
- Fleets = multiple clusters
- Anthos Config Management: Custom policies
- Binary Authorization

## Anthos Bare Metal

"Move the cloud to you."

Deploy applications on your own hardware. Anthos Bare Metal manages app deployment and health + controls security.

Deployment options:

- _Standalone:_ Single cluster. Best for single teams and single workload types
- _Multi-cluster:_ Works well with a fleet of clusters. Multiple teams
- _Hybrid:_ Specialized multi-cluster. Only if no security concerns with user workloads on admin.

Use **Connect** service to associate bare metal clusters to Google Cloud.
