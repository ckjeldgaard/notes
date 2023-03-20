# Anthos

- Application deployment anywhere: GCP, on-premise, hybrid and multi-cloud (AWS and Azure)
- Kubernetes Engine, Cloud Run and VM's
- **Migrate for Anthos**: Migrate existing apps to GKE
- CI/CD automated pipelines

## Anthos Service Mesh

- Manage microservices. Communication of services on-premise and GCP
- Powered by **Istio**
- Controls traffic flow.
    - Support canary and blue-green deployments.
    - Load balancing
    - Monitoring, logging and trace
- Can simulate fault injections like:
    - **Network latency**
    - **HTTP error codes**

## Anthos GKE connection

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
