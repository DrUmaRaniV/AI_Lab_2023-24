# Ex.No: 2  Implementation of Depth First Search
### DATE:                                                                            
### REGISTER NUMBER : 
### AIM: 
To write a python program to implement Depth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function dfs and take the set “visited” is empty 
4. Search start with initial node. Check the node is not visited then print the node.
5. For each neighbor node, recursively invoke the dfs search.
6. Call the dfs function by passing arguments visited, graph and starting node.
7. Stop the program.
### Program:
~~~

graph = {
  '5' : ['3','7'],
  '3' : ['2', '4'],
  '7' : ['8'],
  '2' : [],
  '4' : ['8'],
  '8' : []
}
visited = set()
def dfs(visited, graph, node):  #function for dfs 
    if node not in visited:
        print (node)
        visited.add(node)
        for neighbour in graph[node]:
            dfs(visited, graph, neighbour)
# Driver Code
print("Following is the Depth-First Search")
dfs(visited, graph, '5')

~~~





### Output:

![Screenshot 2024-03-05 213803](https://github.com/ilaya27464/AI_Lab_2023-24/assets/127576283/ac18ad08-ef3a-4667-909b-a8883b7e01a1)

### Result:
Thus the depth first search order was found sucessfully.
