# Operations

Logging, monitoring, error reporting, trace, debug, Profiler (CPU/memory data)

## Logging

- Export logs to other resources
- Exam perspective:
  - IAM roles
  - Exports
  - Logging with other Stackdriver products
- Export (primarily Storage & BigQuery): **Sink**, **filter**, **destination**

Custom metrics can be created from logging and used in monitoring.

Data access logs: Must be enabled

## Monitoring

Exam perspective: Know how to use monitoring with other Stackdriver products

Monitoring of GCP, AWS and third-party apps (must be public and allow firewall traffic from uptime source IP addresses. Typically port 80/443)

## Stackdriver Agent

(installed on VMs)

Uptime check: Can check if a resource is running. Used together with alerts.

## Trace

- Find bottlenecks
- Can be installed outside GCP

## Error reporting

Real-time error reporting

## Debug

Debug apps on GCP

## Profiler

Collect CPU/RAM usage
