# Identity-Aware Proxy

Establishing a central authorization layer to guard access to apps and VMs.

- Controls HTTPS access to apps and VMs on GCP
- Central authorization layer for application-level access control
- Enforces access policies
- Allows employees to work from untrusted networks without VPN

## How it works

1. User hits Cloud IAP proxy
2. Authentication
   - Cloud IAP-enabled app or backend service
   - Valid credentials
3. Authorization
   - Checks if user has authorized access

:::tip OAuth
When IAP is turned on for a resource, it automatically creates an OAuth 2.0 client ID and secret.
:::

## On-premises

IAP can also be used to access resources in-premises. The steps are almost the same as if the resources are in GCP, but after successful authorization:

- The request will be forwarded to Cloud IAP connector
- Forwards the request through Interconnect
  - Site-to-site from GCP to on-prem

## Securing IAP

- Context-Aware Access
- Signed Headers (JSON Web Token (JWT))
- IAP TCP Forwarding (control who can access administrative services til SSH and RDP)
