## How to choose a Database based on the CAP Theorem

#### Examples

- MongoDB
  - Single Master; trades off availability (see point below).
  - Multiple single points of failure.
- Cassandra
  - No single master; eventually consistent.

## How to:
In order to choose a DB you need to understand requirements about scale,
consistency, and availability before choosing one.
