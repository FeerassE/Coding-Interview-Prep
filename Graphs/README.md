
# Graph

## Representations

Graphs can be represented as adjacency lists or as an adjacency matrix.

When the graph is sparse (few edges where |E| is much less than |V|^2) choose adjacency list.

When the graph is dense (lots of edges where |E| is close to |V|^2) choose adjacency matrix.

### Depth First Search (Stack)

Time Complexity: O(|V| + |E|)

```
# Recursive
def dfs(graph, node, visited)
   if visited is None:
      visited = {}
      
   visited[node.val] = True
   for child in graph[node.val]:
      if child.val not in visited:
         dfs(child, visited)

# Iterative (use a stack)
# pop node from stack
# add the last unvisited child to stack
# once all children visited, say node is visited

def dfs(graph, root, visited)
   visited = {}
   stack = deque()
   stack.append(root)
   visited[root.val] = True
   
   while stack:
      node = stack.pop()
      for child in graph[node.val]:
         if child.val not in visited:
            stack.append(child)
            visited[child.val] = True
```
### Breadth First Search (Queue)

Time Complexity: O(|V| + |E|)

```
# Iterative
import queue
def bfs(tree):
   visited = {}
   q = deque()
   q.append(tree)
   visited[tree.val] = True
   
   while q:
      node = q.popleft()
      
      for child in graph[node]:
         if child not in visited:
            q.append(child)
            visited[child.val] = True
```

#### PreOrder, InOrder, PostOrder Traversal (Binary Tree)
Look at where the print statements are.
```
# Preorder Traversal

def traverse(tree):
   if tree:
      print(tree)
      traverse(tree.left)
      traverse(tree.right)
      
# Inorder Traversal
# Use to get the non-decreasing order for a binary search tree

def traverse(tree)
   if tree:
      traverse(tree.left)
      
      print(tree)
      traverse(tree.right)
      
# Postorder Traversal

def traverse(tree)
   if tree:
      traverse(tree.left)
      traverse(tree.right)
      print(tree)
```
