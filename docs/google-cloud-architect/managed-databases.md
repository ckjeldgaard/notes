# Managed databases

_Horizontal_ vs. _vertical_ scaling:

- _Horizontal_: Scaling out. Add more machines
- _Vertical_: Scaling up. Add more compute to 1 machine

OLTP = Online Transaction Processing (Transactional)

OLAP = Online Analytical Processing (Analytical)

<table>
  <thead>
    <tr>
      <th>Database</th>
      <th>Type</th>
      <th>Use case</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Cloud Spanner</td>
      <td>Relational</td>
      <td>Scale, high transactions</td>
    </tr>
    <tr>
      <td>Cloud SQL</td>
      <td>Relational</td>
      <td>Structured data, MySQL or PostgreSQL</td>
    </tr>
    <tr>
      <td>Datastore</td>
      <td>Non-SQL</td>
      <td>Key-value data</td>
    </tr>
    <tr>
      <td>Cloud Bigtable</td>
      <td>Non-SQL</td>
      <td>High throughput, analytics</td>
    </tr>
    <tr>
      <td>BigQuery</td>
      <td>Data warehouse</td>
      <td>Analytics of big data</td>
    </tr>
  </tbody>
</table>

Cloud Memorystore = Redis
Filestore = NAS

## Cloud SQL

By default, Cloud SQL = Single VM instance

Replicas:

- Read replica
- Failover replica

## BigQuery

Exam: Managing resources and users

- Query history / Job history
- Partition tables to reduce costs + improve performance. Methods:
  - Ingest time
  - Timestamp
- Set expiration on data
