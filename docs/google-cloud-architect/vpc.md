# VPC

Virtual version of a physical network.

Software-Defined Network (SDN)

:::tip Note
VPC is **global**, but the subnets are **regional**. Can have single subnet span multiple zones.
:::

- VPC can have both _external_ and _internal_ IP addresses
- Hybrid networking with on-premises networks with interconnect options

## Firewall

- Implied `denied all` ingress
- Implied `allow all` egress

Conditions for determining access:
Source/target, protocols, ports, tags

## Shared VPC

May need to share network resources across projects.

Terminology:

- Host project
- Service project
- Standalone project
- Shared VPC Admin
- Service project admin

Only within single organization.

## VPC modes

- Auto mode
- Custom mode
