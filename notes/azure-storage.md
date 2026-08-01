---
title: Azure Storage
tags: [azure, azure-developer-associate, cloud, storage]
up: "[[azure]]"
---

# Azure Storage

## Configuring Azure Blob Storage
### Standard vs premium
- Premium isn't premium, it is just to mount storage for virtual machines.
### Redundancy
- Locally-redundant-storage (LRS): Lowest-cost option with basic protection against server rack and drive failures. Recommended for non-critical scenarios.
- Geo-redundant-storage  (GRS): Intermediate option with failover capabilities in a secondary region. Recommended for backup scenarios.
- Zone-redundant storage (ZRS): Intermediate option with protection against datacenter-level failures. Recommended for high availability scenarios.
- Geo-zone-redundant storage (GZRS): Optimal data protection solution that includes the offerings of both GRS and  ZRS. Recommended for critical data scenarios.
### Security
- Require secure transfer for REST API operations.
- Allow enabling public access on individual containers.
- Enable storage account key access.
### Networking
- Enable access for all networks.
- Enable public access from selected virtual networs and IP 
### Data protection
If your blob storage involves frequent changes by multiple users then soft delete and point in time restore are good options.
For even more granular control, you can enable versioning on blobs but be aware that this could get spendy.
You can also enable blob change feed to track changes on blob on account, which is handy in event driven scenarios.
### Encryption
- Handle encryption on data inside the blob storage.
- Data at rest using Storage Service Encyption (SSE).
- Data in transit with client-sice encyption HTTPS or SMB 3.0.
- OS and data disk using Azure Disk Encryption.
- Infrastructure encryption on top of service-level encryption.
- Keys: Microsoft-managed, customer-managed, customer-provided.

### Container Naming
- The name doesn't need to be universally unique, only unique within your storage account.
### Container access level
- Private  (no anonymous access)
- Blob (anonymous read access for blobs only)
- Container (Anonymous read access for containers and blobs)
### Blob types
- Block: General-use storage for text and binary data. Made up of blocks of data that can be individualy managed by ID. Max blob size is 5 gib to 190 tib depending on the PUT method. (Hot, Cool, Cold, Archive) tiers.
- Append: Like block blobs but better optimized for append operations like logging. Each append blob is made up of up to 50000 blocks with non transaparent IDs. The max blob size is 195 gib. (Doesn't have storage tiers).
- Page: Used for random access files. Used primarily for virtual hard drive (VHD) files. Max blob sixe is 8 tib. (Doesn't have storage tiers).
#### Tiers
- Hot: default, frequent access.
- Cool: accessed every 30-90 days.
- Cold: minimum 90 days.
- Archive: must rehydrate, 180 days minimum.
The hotter the tier the lower are the transfer rates, but the cooler the tier have lower storage rates.
### Lifecycle Management Policies
Are used to automatically transition data between different storage tiers depending on the age of the data. This helps balancing the cost and accessibility requirement of stored data, ensuring that requently accessed data is quickly available while less frequently accessed data is stored more cost-effectively.
### Managing properties with REST API
Example of blob storage base url:
https://storage-account/blob.core.windows.net
From there both GET and HEAD operations can retrieve metadata. 

GET/HEAD https://storage-account/blob.core.windows.net/yourcontainer?restype=container
Here you can obtain metadata from your container. You can also override metadata using the PUT command.

GET/HEAD https://storage-account/blob.core.windows.net/yourcontainer/ablob?comp=metadata
Here you can obtain the metadata from your blob.

## Related

- [[azure-authentication-authorization]] — SAS tokens and the Storage Blob RBAC roles.
- [[azure-cosmos-db]] — the NoSQL database alternative for structured data.
- [[azure-functions]] — blob and queue triggers.
- [[azure-container-instance]] — Azure Files for persistent container storage.
- [[information-extraction]] — where extracted document data often lands.
- [[exam-questions]] — tiers, blob types, lifecycle policies, and `$web` all appear here.
