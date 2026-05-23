## Promises of Cosmos DB
- Cosmos db can be globally distributed across the world.
- The closer the users are to the data source, the faster the responses will be.
- This is a mulitmodel NoSQL database.
- Guaranteed single-digit millisecond response times.
- 99.99% availability.
- Backed by service level agreements (SLAs).
- Automatic and instant scalability.
- Multi-master global distribution.
- One-year free tier.
## Understanding Request Units
Cosmos db throughput is measured by (CPU, Memory and IOPS) that are consumed when making a request to a cosmodb database.
## Types of Cosmosdb
- JSON/BSON: Native or MongoDB
- Wide column, Key-Value: Apache Cassandra, Table (Azure Table storage)
- Graph: Apache Gremlin
- Distributed tables: PostreSQL (Citrus extension)
## Setting Partition Schemes and Keys 
#### Logical Partitions
These are formed based on the value of a partition key.
- Logical Model < Account < Databases < Containers (Logical parition with chunkof data)
- Each container has a different partition key.
#### Physical Partitions
Are the internal implementation of the system and are entirely managed by cosmosdb. Internally one or more logical partitions are mapped to a single physical partition. The platform handles the distribution of logical partitions across physical partitions automatically.
### Types of keys
- Partition keys: Can be strings or numeric types. The partition key is critical as it determines how data is distributed across logical partitions.
- Item IDs: Each item in a container has an item id (unique within a logical partition). The partition key combined with the unique key guarantess the uniqueness of an item within the scope of the container.
- Unique keys: Ensures that one or more values within a logical partition are unique. The partition key combined with the unique key guarantees the uniqueness of an item within the scope of the container.
## Consistency Models
Offers five well defined consistency levels.
- Strong consistency: Guarantees that the most recent committed version of the data will be returned. It's used when you can't compromise the user seeing tentative or outdated changes on the data. Reads are guaranteed to read the most recent committed version of an item. Clients will never see a partial or an uncommitted write.  (Single source of truth).
- Eventual Consistency: Does not guarantee any ordering and only ensures that replicas will eventually converge. (Promises that eventually everyone will see the same information).
- Consistent Prefix: Adds ordering guarantees on top of eventual consistency. This means that if you see write operations A, B and C, you will never see A and C without seeing B, preserving the order of operations.  (Ensures that you see things in the correct order).
- Bounded Staleness: Adds time and operation bounds on top of consistent prefix. When configured reads are guaranteed to have a staleness (expiration time) less than the configured bounds. Allows you to configure how far begind reads can be in terms of operations. (Like agreeing that you are ok with seeing information that is slightly outdated).
- Session consistency: Is the default level applied to CosmosDB. When working with session consistency each new write request to azure cosmosdb is assigned a new session token. This level of consistency honors the client session. It ensures strong consistency for an application session with the same session token. (Ensures that if you make a change, you'll always see your own changes, you'll always see what you wrote but others might see an older version).
