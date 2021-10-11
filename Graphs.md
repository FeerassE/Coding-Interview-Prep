
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
# Recursive (need to check if this is correct)
import queue
def bfs(node, queue):
   for child in node.children:
      queue.put(child)
   
   if len(queue):
      bfs(queue.get(),queue)

# Iterative
import queue
def bfs(tree):

   queue = queue.Queue()
   queue.put(tree)
   
   while(len(queue)):
      node = queue.get()
      
      for child in node.children:
         queue.put(child)
```

#### PreOrder, InOrder, PostOrder Traversal
Look at where the print statements are.
```
# Preorder Traversal

def traverse(tree):
   if tree:
      print(tree)
      traverse(tree.left)
      traverse(tree.right)
      
# Inorder Traversal

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
