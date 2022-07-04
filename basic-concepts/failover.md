## Failover

## Failover Strategies

### Databases - Cold Standby

Is the idea of having a "close to ready" state instance, that will be used in the case of the main host going down.
It is commonly used with periodic backups, and the only downside is that you need to wait for it to restore the 
latest backup of the data to get it to a ready state, and then be able to redirect the traffic to that instance.

- Pros
  - Cheap and simple
- Cons
  - Need to wait for the backup to be restored.
  - Any data from after the last backup will be lost.
  - Data loss is inevitable
  - Is vertical scaling

### Databases - Warm Standby

Is the idea of having a replicated instance that will have an almost real-time copy of the data.

- Pros
  - Ready to go, almost instant and most of the time automatic
  - Fairly simple
- Cons
  - Data loss could happen
  - Increased load on the backup instance
  - Is still vertical scaling

### Databases - Hot Standby

Instead of using replication of the data, the idea is to write simultaniously to all instances.

- Pros
  - Can distribute the read
  - Almost horizontal scaling
- Cons
  - No dataloss
  - Load is are affecting all instances

### Databases - Sharding

![image](https://user-images.githubusercontent.com/36679293/177078208-2ec4fe1a-3c87-401a-9d86-0e03c65afccc.png)

A shard is a horizontal partition of the database. Each shard has a backup.
In a sense, there is hot standbys.

- Pros
  - Each shard has a backup
  - Redirects to shards
- Cons
  - Data merging or joins are a complicated task

#### Example

- MongoDB
  - "mongos" is the shard load balancer
    - Redirects data and requests to the shards depending on a set scheme
  - Each shard has a primary server and multiple secondary (backup) servers. Usually called replica sets
    - Primary servers can be replaced automatically by the secondary servers.
  - The database has a scheme for the config. A config server, and two secondary config servers are in charge of defining that scheme.

![image](https://user-images.githubusercontent.com/36679293/177079324-15bfd3e2-d49e-47b7-83c9-690129713a3e.png)

- Cassandra
  - Has a node ring system where the data is still sharded, but any of the nodes can serve as a primary node.
  - All of the nodes need to know how has what and where.
  - "Eventual consistency" is a tradeoff, because it takes time to sync everything.

__Sharded databases are usually called NoSQL__

