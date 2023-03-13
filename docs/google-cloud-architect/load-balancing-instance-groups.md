# Load balancing & instance groups

## Load balancer

Distributes user network requests among a pool of instances

> Single **frontend** access = Multiple **backend** targets

### Load balancer types

<table>
  <tbody>
    <tr>
      <td rowspan="4">External</td>
      <td>HTTP(S) - layer 7 LB</td>
      <td rowspan="3">Global</td>
    </tr>
    <tr>
      <td>SSL proxy</td>
    </tr>
    <tr>
      <td>TCP proxy</td>
    </tr>
    <tr>
      <td>Network load balancer</td>
      <td rowspan="2">Regional</td>
    </tr>
    <tr>
      <td>Internal</td>
      <td>Internal load balancer (TCP/UDP)</td>
    </tr>
  </tbody>
</table>

- Forwaring rules . By **location** ("US or Asia?") or **content** ("Video or not video?")
- HTTP load balancer - layer 7
- Network load balancer - layer 4

### Regional load balancing features

- Health checks
- Session affinity
- IPv4 only

### Global load balancing features

- Multi region
- Connects to closest region
- IPv4 and IPv6

## Instance groups

- Automatically scales
- Work with load balancers
- How it works:
  - **Global:** _a._ Create instance template
  - **Regional:** _b._ Create instance group from template
- Instance group is **regional** - not global

Sole-tenant VMs support BYOL situations.

## Health checks

- Auto-healing
- If an instance fails -> Delete and recreate identical one

:::tip Mental model
Pets vs. livestocks (cattle)
:::

Can use startup script or custom image to create instance template.

- **Startup script**
  - Easy to create
  - But longer wait until ready
- **Images**
  - More involved setup
  - But VM is ready right away

Use managed instance group updater to update! Replaces individual VM's
