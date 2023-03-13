---
sidebar_position: 3
---

# Mountkirk Games

- Makes online multiplayer games for mobile platforms
- Expanding to other platforms. Is on GCP

## Concerns

- New multiplayer game on GKE
- Use global load balancer to keep latency down
- Global real-time leader board (rely on streaming data)
- Use _Cloud Spanner_ as database

## Existing

5 games on GCP
Some legacy games

**Recommended for GDPR: Cloud EKM (External Key Manager), Cloud DLP (Data Loss Prevention)**

## Business requirements

- Support multiple platforms (could be backends)
- Multiple regions
- CI/CD model
- Minimize latency
- Managed services
- Minimize costs

## Technical requirements

- Scale based on game activity
- Leaderboard (streaming data)
- Logs in structured files (Dataflow for analysis)
- Use GPU processing to render graphics server-side **(Spot VM's with GPU node pools)**
- Eventually migrate legacy games to new platform

## Summary

- Other gaming platforms + other regions
- Tech:
  - Kubernetes
  - Load balancer
  - Cloud Spanner
- Latency top priority - and cost close second **(For latency recommend: Cloud Trace, Cloud Profiler. Don't recommend Cloud Monitoring, Web Security Scanner)**

:::tip Note
For compliance: Compliance Report Manager
:::
