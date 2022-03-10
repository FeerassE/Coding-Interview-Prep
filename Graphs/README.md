
# Graphs

### Depth First Search (Stack)

Time Complexity: O(|V| + |E|)

```
# Recursive
def dfs(node, visited)
   if visited is None:
      visited = set()
      
   visited.add(node)
   
   for child in node.children:
      dfs(child, visited)

# Iterative (use a stack)
# pop node from stack
# add the last unvisited child to stack
# once all children visited, say node is visited

# this needs TESTING
def dfs(tree, visited)
   visited = set()
   stack = [tree]
   
   while(len(stack)):
      node = stack.pop()
      for child in node.children:
         if child not in visited:
            stack.append(node)
            stack.append(child)
            continue
      visited.add(node)
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
      
      for child in node.children:
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
