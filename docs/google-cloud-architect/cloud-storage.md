# Google Cloud Storage

Storage of files in the cloud.

- Pay per use, not allocation
- Objects = files

Storage classes:

<table>
<thead>
<tr>
<th>Storage class</th>
<th>Minimum storage duration</th>
<th>Retrieval fees</th>
</tr>
</thead>
<tbody>
<tr>
<td>Standard</td>
<td>None</td>
<td>None</td>
</tr>
<tr>
<td>Nearline</td>
<td>30 days</td>
<td>Yes</td>
</tr>
<tr>
<td>Coldline</td>
<td>90 days</td>
<td>Yes</td>
</tr>
<tr>
<td>Archive</td>
<td>365 days</td>
<td>Yes</td>
</tr>
</tbody>
</table>

## gsutil

Syntax: `gs://<BUCKET_NAME>/<OBJECT_NAME>`

`gsutil <command> <option> <target>`

Example:

`gsutil cp file1.txt gs://mybucket`

Like Linux: `cp`, `mv`, `rm`, `ls`...

## Security

Two methods:
- IAM
- ACL (Access Conrol Lists). Some overlap. Can be applied to bucket or individual objects

Best practice is to use IAM over ACL. IAM leaves audit trails for access.

**Signed URL** - Timed access to object data. Setting a timer to non-Google account

By default, GCP encrypts all data.

Customer can manage own keys - then using `.boto` config file

:::tip Security marks
Add security marks to any Cloud Storage buckets to identify buckets outside of policy. Security marks are only visible through the Cloud Security Command Center which would keep the information classified and actionable. 
:::

## Bucket locations

- **Region**: a specific geographic place, such as São Paulo.
- **Dual-region** : a specific pair of regions, such as Tokyo and Osaka.
- **Multi-region**: a large geographic area, such as the United States, that contains two or more geographic places.

## Object versioning

- Retrieve older versions of objects
- Disabled by default
- Considerations:
  - Cost
  - Retains own ACL

## Object lifecycle management

- Sets time to live (TTL) on an object
- Applied on bucket
- Often used with versioning
- _Rules_, _conditions_, _actions_
  - Delete
  - Set storage class
