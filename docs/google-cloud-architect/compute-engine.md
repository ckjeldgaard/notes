# Compute Engine

Virtual Machines

Disks:
- Persistent disks
- Local SSD
- Cloud Storage buckets

Committed use discount can be purchased for VMs.

## Persistent disk

- Very flexible and powerful - less physical constraints - **Modular!**
- Default
- Array of multiple disks (not a physical disk, but exists in the network)
- Modular
- SSD persistent disk

## Local SSD

- Highest performance, but with caveats
- Cannot be boot
- **375GB** in size - non-configurable

## Cloud Storage bucket

- Niche use case
- Act as-if it was a real disk
- Not block storage (is object storage)

## Images

- **Public** and **custom**
- Not limited to zone
- Necessary to create boot disks on GCE instances
  - Image: Create new instance
  - Snapshot: Backup

## Snapshots

- Backup of disk
- Share across projects
- Periodic backups via a point in time snaphot of disk
  - Incremental backups
    1. First snapshot full disk copy
    2. Subsequent snapshots are only what's different compared to previous snapshot.

## Startup and shutdown scripts

- For automation!
- Always run as root
- Two input methods
  - Direct
  - Link to script in Storage

Shutdown:

- Best effort basis
- May shut down before script completes

## Preemptible VM's

- Can be purchased for a steep discount as long as customer accepts that the instance will **terminate after 24 hours**.
- Best for:
  - Testing
  - Batch jobs
  - Fault tolerant apps
