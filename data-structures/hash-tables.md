## Data Structures: Hash Table

#### Features
- A "hash function" quickly maps some key to a bucket.
- That bucket is then searched for the key's value.
- Writes, Reads and Deletes are O(1) in average, but O(n) in the worst case.

#### Cons
- Hash collisions occur when more than one key maps to the same bucket.

#### Usecases
- Distributing reads across a handful of servers (finding which server has the information) 
