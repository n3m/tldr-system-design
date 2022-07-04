## Horizontal Scaling

Horizontal scaling is the process of creating more instances of the same type to split up the load (requires a load balancer). This solution doesn't have a single point of failure and instead adds redundancy (assuming that we have enough capacity provisioned).

- Pros
  - No downtime
  - Redundancy
- Cons
  - Management becomes difficult
  - Only works well if the entities are stateless.

## Vertical Scaling

Vertical scaling refers to the process of assigning more resources to the instances (aka making them bigger/beefier) in order for them to take more data in.
To some extent this works, but it can only take you to a certain point before becoming a very expensive solution or by hitting the hardware limits, and still creates a single point of failure without proper redundancy.

- Pros
  - Fewer servers to maintain
- Cons
  - Single points of failure everywhere

### Example

#### Single-Server Design

Just a single entity that manages all requests and just scales (vertically) in size whenever needed.
An example is a home-based NAS Server.

Pretty much a design for unimportant and small scale problems.
