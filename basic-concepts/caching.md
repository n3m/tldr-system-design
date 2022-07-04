## Caching

The action of storing a frequently accessed piece of information in a reliable and fast storage for quick access.

## Caching Strategies

### Caching Layers

- A fleet of entities that have a sole job of keeping copies of frequently accessed resources in memory to avoid bottlenecks.
- Require expiration policies that dictate how long the data is cached.
- The clients hash request to a given server

- Pros
  - Horizontally Scaled Servers
  - In-memory
  - Severily improves performance (commonly used for Databases)
- Cons
  - Hotspots can be created. (Smart caching can be a solution)
  - Cold-starts are an issue. (How do you start a cache layer without DDoS'ing yourself?)

- Usecases
  - Applications with more reads that writes

### Eviction Policies

- LRU: Least Recently Used
  - The oldest data will be kicked out of the data
- LFU: Least Frequently Used
- FIFO: First In; First Out

__LRU Example__

![image](https://user-images.githubusercontent.com/36679293/177084848-7b7b083e-0973-4b17-98b4-5342dd8aad7f.png)

## Caching Tecnologies

- Memcached
  - In-memory key/value store
  - Open source
- Redis
  - Snapshots, replication, transactions, pub/sub
  - Advanced datastructures
  - Complex but reliable
- Ncache
  - Made for .NET, Java, Node.js 
- Ehcache
  - Just a distributed map
- ElastiCache
  - AWS Solution
  - Fully-managed Redis or Memcached
