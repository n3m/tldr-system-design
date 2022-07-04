## Resiliency

"What happens when things go wrong?"

Concept for managing solutions for system or general failures.

### Things that can fail

- Single server
- Rack of servers
- Data Centers / Availability Zones
- Entire Regions

### How?

- Use Geo-Routing with DNS or some service that detects regions and regions availability to redirect requests
- Spread the system architecture across multiple racks, availability zones, and regions
- Make sure that the whole system has capacity to survive a failure at any reasonable scale.
  - Need to take into account overprovisioning. 
