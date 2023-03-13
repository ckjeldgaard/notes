---
sidebar_position: 4
---

# TerramEarth

- Heavy equipment, mining, agriculture
- 500 dealers in 100 countries

## Concerns

- 2 million vehicles
- Collect data from sensors (IoT)
- Some is streaming - other compressed and uploaded daily
- 200-500 MB data per vehicle per day
- Private Data Center Integration with multiple network interconnects to Google Cloud

## Business requirements

- Predict malfunctions
- Decrease costs seasonality
- Increase speed+reliability (SRE)
- Allow remote developers (IAM roles)
- API for dealers and partners

## Technical requirements

- Abstraction layer API for legacy systems
- CI/CD pipelines for containers (Kubernetes, Cloud Run + Cloud Build)
- Allow devs to experiment (test environments on test GCP project)
- Self-service web portal (web project with access to spin up new projects with access to **BigQuery** and perhaps **controlling network gateways** with network tags)
- IAM, security manager, KMS
- Monitoring, logging, debugging

## Summary

- Customer and partner support
- Expand global integration
- Transmit and analyse data
