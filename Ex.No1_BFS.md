# Ex.No : 1  Implementation of Breadth First Search 

### DATE
- 17/02/2024                                                                            

### REGISTER NUMBER
- 212221040116 

### AIM
- To write a python program to implement Breadth first Search. 

### ALGORITHM
- Start the program.
- Create the graph by using adjacency list representation.
- Define a function bfs and take the set “visited” is empty and “queue” is empty.
- Search start with initial node and add the node to visited and queue.
- For each neighbor node, check node is not in visited then add node to visited and queue list.
- Creating loop to print the visited node.
- Call the bfs function by passing arguments visited, graph and starting node.
- Stop the program.

### PROGRAM
```
graph = {
  '5' : ['3','7'],
  '3' : ['2', '4'],
  '7' : ['8'],
  '2' : [],
  '4' : ['8'],
  '8' : []
}
visited = set()
def dfs(visited, graph, node):
    if node not in visited:
        print (node)
        visited.add(node)
        for neighbour in graph[node]:
            dfs(visited, graph, neighbour)

print("Following is the Depth-First Search")
dfs(visited, graph, '5')
```

### OUTPUT
![image](https://github.com/DrUmaRaniV/AI_Lab_2023-24/assets/114301782/ed66aefe-69d4-4741-af27-81c06d7e9719)


### RESULT
Thus the breadth first search order was found sucessfully.
