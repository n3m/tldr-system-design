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





