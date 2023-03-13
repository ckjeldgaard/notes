# Cloud IAM

Who = Member
Can do what = Role
On Which Resource = All resources on GCP

Role != permission

Role _has_ permission

## Google account types

- Personal
- GSuite domain (+ Google apps)
- Cloud Identity Domain (- Google apps)
- Google Group (Collection of Google accounts)
- allAuthenticatedUsers
- allUsers
- Service accounts

### Cloud identity

> Sync with active directory (AD)

- Cloud identity maps (federates) AD accounts to Cloud Identity Accounts
- How to sync
  - Google Cloud Directory Sync (GCDS)
  - Active Directory Federation Services (ADFS)

## Role types

- Primitive
  - Owner
  - Editor
  - Viewer
- Predefined
  - E.g. `compute.instanceadmin`
- Custom roles

:::tip Binding
Binds a list of **members** to a **role**.
:::

Organization administrator role very powerful.

## Service accounts

Types:

- Google managed (generally invisible to user)
- User-managed (created for/by user)

Both a member and a resource

- Service accounts are granted permissions to a service
- Users (person) are granted role serviceAccountUser to a service account

Service account keys = Kind of passwords for SA's

Service account scopes = legacy

## IAM best practices

- Least privilege
  - Predefined roles over primitive
  - Restrict access to service accounts
- Rotate service account keys (if custom)
- Use Cloud Audit logs to audit IAM changes
- When possible, use groups
- More than one org admin

## Billing overview

- Assigned mostly at org level
- Billing data can be exported to Cloud Storage and BigQuery
- Set budget and alerts
- Billing account roles:
  - Creator
  - Administrator
  - User (often with creator)
  - Viewer
  - Project billing manager
