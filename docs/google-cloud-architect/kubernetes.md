---
sidebar_position: 2
---

# Kubernetes

Exam tests deployment process

- "Build it"
- Container Registry - "Store it"
- Kubernetes Engine - "Deploy and run it"

## Terminology

- **Node:** VM's containers are hosted on
- **Node pool:** Group of nodes
- **Cluster:** One or more node pools
- **Node image:** Node-level OS image
- **Pods:** Smallest deployable unit
- **Container image:** Base image used in container

## Dictionary

- **Deployment:** Stateless applications
- **StatefulSets:** Stateful apps. Persistent ID for each pod
- **DaemonSets:** One pod per node (background tasks)
- **ConfigMap:** Env vars, CLI args etc. to containers at run-time
