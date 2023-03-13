# Networking

Extending _your_ network to Google's network.

- Cloud Interconnect
- Cloud VPN
- Peering

## Cloud Interconnect

**80 GB**

- Physically connect (high volume process)

## Cloud VPN

**12 GB**

- Option for most of us
- Connect to GCP over encrypted tunnel over public internet
- VPN over IPSec
- Static and dynamic routes (using Cloud Router)

:::tip Cloud VPN Gateways
Cloud VPN Gateways are bound to a single region!
:::

## Peering

- Connect to Google (not just GCP) over public internet
- Not exam relevant

## Cloud DNS

- Public/private DNS zones
- Each domain has own zone
