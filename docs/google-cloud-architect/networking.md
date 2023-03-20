# Networking

Extending _your_ network to Google's network.

- Cloud Interconnect
- Cloud VPN
- Peering

## Cloud Interconnect

**80 GB**

- Physically connect (high volume process)
- Use when you want to prevent traffic from traversing the public internet
- Can be used with Private Google Access (RFC 1918). This way internal IP addresses can be used rather than external IP addresses to reach Google APIs and services.
- Speeds from 50 Mbps - 200 Mbps
  - **Dedicated:** 10 Gbps link (up to 8) or 100 Gbps link (up to 2). Must install and maintain your own _routing equipment_.
  - **Partner:** 50 Gbps - 10 Gbps
- Egress savings

## Cloud VPN

**12 GB**

- Option for most of us
- When public internet access is needed
- Connect to GCP over encrypted tunnel over public internet
- VPN over IPSec
- Static and dynamic routes (using Cloud Router)
- Supports up to 3 Gbps per tunnel (8 tunnels max)

:::tip Cloud VPN Gateways
Cloud VPN Gateways are bound to a single region!
:::

## Peering

- Connect to Google (not just GCP) over public internet
- Not exam relevant

## Cloud DNS

- Public/private DNS zones
- Each domain has own zone
