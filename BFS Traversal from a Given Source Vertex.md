# Ex. No: 17B - BFS Traversal from a Given Source Vertex
# AIM:
To write a Python program to print BFS traversal from a given source vertex.

# ALGORITHM:
Step 1: Start the program.

Step 2: Create a graph using adjacency list representation.

Step 3: Add edges between vertices using the addEdge() method.

Step 4: Implement the BFS() function:

Initialize all vertices as not visited.
Use a queue to track vertices for traversal.
Mark the starting vertex as visited and enqueue it.
Dequeue a vertex, process it, and enqueue all its adjacent unvisited vertices while marking them as visited.
Step 5: Input the starting vertex and perform BFS traversal from it.

Step 6: Print the vertices in BFS order.

Step 7: End the program.

# PYTHON PROGRAM
~~~
Reg.No: 212222060229
Name: Sarvesan lathika

from collections import defaultdict

class Graph:

	def __init__(self):

		self.graph = defaultdict(list)
	def addEdge(self,u,v):
		self.graph[u].append(v)

	def BFS(self, s):
		visited = [False] * (max(self.graph) + 1)
		queue = []

		queue.append(s)
		visited[s] = True
		while queue:
		    s=queue.pop(0)
		    print(s, end=' ')
		    for i in self.graph[s]:
		        if visited[i]==False:
		            queue.append(i)
		            visited[i]=True

n=int(input())
g = Graph()
g.addEdge(0, 1)
g.addEdge(0, 2)
g.addEdge(1, 2)
g.addEdge(2, 0)
g.addEdge(2, 3)
g.addEdge(3, 3)

print ("Following is Breadth First Traversal"
				" (starting from vertex {})".format(n))
g.BFS(n)
~~~
# OUTPUT
<img width="1174" height="213" alt="image" src="https://github.com/user-attachments/assets/a6c4ba00-855d-45cc-a7df-78059dc21be6" />

# RESULT
Hence, The program is successfully executed and the Breadth First Search (BFS) traversal from the given source vertex is verified.
