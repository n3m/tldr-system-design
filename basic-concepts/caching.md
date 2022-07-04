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
  - Hotspots can be created.
  - Cold-starts are an issue. (How do you start a cache layer without DDoS'ing yourself?)

- Usecases
  - Applications with more reads that writes
