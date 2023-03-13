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
- Legacy integrations with insurance on-premise
- Users managed with Microsoft AD

## Business requirements

- Onboard new insurance ASAP
- Minimum 99.9 % availability (SLA)
- Centralized visibility **(logging, monitoring)**
- Insights to healthcare trends (most likely AI + BigQuery)
- Reduce latency
- Maintain compliance
- Decrease costs
- Make predictions

## Technical requirements

- Maintain latency interfaces (Anthos!)
- Managed containers (Kubernetes, K8S Anthos)
- Secure connection
- Consistent logging
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
