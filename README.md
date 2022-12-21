# AI-ML## BFS 

# graph = {
# '1' : ['2','10'],
#  '2' : ['3','8'],
#  '3' : ['4'],
#  '4' : ['5','6','7'],
#  '5' : [],
#  '6' : [],
#  '7' : [],
#  '8' : ['9'],
#  '9' : [],
#  '10' : []

# }
graph = {
   's': ['a','d'],
   'a' : ['b'],
   'd' : ['g'],
   'b' : ['c'],
   'c' : ['g'],
   'g' : []
}

visited = [] # List for visited nodes.
queue = []     #Initialize a queue

def bfs(visited, graph, node): #function for BFS
  visited.append(node)
  queue.append(node)

  while queue:          # Creating loop to visit each node
    m = queue.pop(0) 
    print (m, end = " ") 

    for neighbour in graph[m]:
      if neighbour not in visited:
        visited.append(neighbour)
        queue.append(neighbour)

# Driver Code
print("Following is the Breadth-First Search")
bfs(visited, graph, 's') 
