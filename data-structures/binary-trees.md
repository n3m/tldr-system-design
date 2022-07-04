## Data Structures: Binary Trees

#### Features
- Each element has a left and right child
- If the left and right are ordered, then it is called a BST (Binary Search Tree)
- On a perfectly balanced BST > read is O(log(n)) on average | O(n) on worst case
  - Basically we're dividing our search space in half every time, and that cuts time.
- Write is O(log(n)) due to rearranging in the best case and O(n) in the worst case.


#### Usecases
- Mostly used in cases where you need to do in-order traversals

#### Applications
- If your expecting to read a lot more than writing in a binary tree, then using a self-balancing BST would be the best case scenario.
