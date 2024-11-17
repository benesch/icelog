# Icelog

<img src="https://github.com/user-attachments/assets/963f9705-c65a-46fa-abd0-85df4cd9f6fe" alt="icelog logo" width="600">

Icelog is a [catalog implementation] for [Apache Iceberg] that uses nothing
but object storage (e.g., Amazon S3, Google Cloud Storage).

## Motivation

Existing catalog implementations for Iceberg typically require a relational
database to durably record the data in the catalog--i.e., the information
about which tables are stored at which locations in object storage. 

Icelog is different. It stores its catalog data directly in object storage.
It builds atop the object storage primitive of "conditional writes"[^1] 

## Quickstart


[^1]: While conditional writes have been available in Google Cloud Storage and Azure Blob Storage for years, Amazon S3 only added support for them in [mid-2024](https://aws.amazon.com/about-aws/whats-new/2024/08/amazon-s3-conditional-writes/).

[catalog implementation]: https://iceberg.apache.org/concepts/catalog/
[Apache Iceberg]: https://iceberg.apache.org/
