---
sidebar_position: 1
---

# EHR Healthcare

Electronic Health Records

- SaaS for multi-national medical offices, hospitals and insurance providers
- Lots of **compliance**!
- Growing exponentially
  - Needs to scale
  - Disaster recovery plan
  - New CI/CD

## Existing

- Multiple co-locations. One to expire
- Web-based
- Kubernetes containers (MySQL, MSSQL, Redis, MongoDB)
- Legacy integrations with insurance on-premise (to be replaced)
- Users managed with Microsoft AD

## Business requirements

- Onboard new insurance providers ASAP
- Minimum 99.9 % availability (SLA)
- Centralized visibility **(logging, monitoring)**
- Insights to healthcare trends (most likely AI + BigQuery)
- Reduce latency
- Maintain compliance
- Decrease infrastructure administration costs
- Make predictions (AI/ML)

## Technical requirements

- Maintain latency interfaces (answer: Anthos!)
- Managed containers (Kubernetes, K8S Anthos)
- Secure connection
- Consistent logging, monitoring and alerting
- Ingest data from new providers (Dataproc or Dataflow)

## Summary
 
- Compliance
- Legacy
- Security

## Exam notes

- Migrate from MongoDB -> Firestore
- Use Partner Interconnect
- Use **API** for legacy data interface for insurance providers
- Migrate MSSQL -> Cloud Spanner
- Migrate legacy API's in containers -> Migrate for Anthos and GKE
- Move on-prem website to GCE + Cloud Armor and HTTP(S) load balancer to address DDoS issues
- In order to ensure personal data doesn't leave a certain region in Cloud Storage: Use **Virtual Private Network Service Controls**, and create a **service perimeter** around the Cloud Storage resources. 
