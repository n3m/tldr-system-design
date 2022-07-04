## Linked Lists

### Singly Linked List

#### Features
- Grows dynamically
- Each node has a "previous pointer"
- Read is O(n) - aka Linear
- Write at HEAD is O(1) - aka Constant
- Write at END is O(n) - aka Linear
- Low memory usage

#### Usecases
  - Sequential access
  - Stacks & Queues
  - Tail tracking

### Double Linked List

#### Features
- Each node has a "next" and "previous pointer"
- Write is O(1)
- Read is O(n)

#### Usecases
- Useful for Deques
- MRU (Most Recently Used) Caches
