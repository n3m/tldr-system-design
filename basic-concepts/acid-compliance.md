## ACID Compliance

## A - Atomicity
Either the entire transaction succeeds, or the entire thing fails.

#### Example
In SQL there are transactions that can be made up of multiple write operations; 
if one of those operations fails, the whole transaction will fail and the data will be rolled back.

## C - Consistency
All database rules are enforced, or the entire transaction is rolled back.

NOTE: Consistency outside of ACID is usually refering to how fast we can access the data that we just wrote; deriving in "eventual consistency"

## I - Isolation
No transaction is affected by any other transaction that is stil in progress. (If needed, then we need a querying system)

## D - Durability
Once a transaction is commited, it stays, even if the sustem crashes immediately after.

- - - -

"__Sometimes you need to trade the compliance in order to achieve scalability__"


## CAP Theorem

There are three things that we care about databases.
- Availability
- Consistency
- Partition-Tolerance

![image](https://user-images.githubusercontent.com/36679293/177081989-a144495c-a3ab-4c2c-8eee-c18b8c5a6b6e.png)
