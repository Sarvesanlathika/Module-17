Ex. No: 17E - Topological Sorting of a DAG
AIM:
To write a Python program to print topological sorting of a Directed Acyclic Graph (DAG).

ALGORITHM:
Step 1: Create a graph and add edges to represent relationships between nodes.

Step 2: Use a visited set to keep track of visited nodes and a stack (or list) to record the order of nodes after processing.

Step 3: Perform DFS for each unvisited node:

Explore all its neighbors. Recursively apply DFS to each unvisited adjacent node. After all neighbors are visited, push the current node onto the stack. Step 4: After DFS is complete for all nodes, the stack will contain nodes in reverse order of their completion time.

Step 5: Print the stack in reverse to get the topological order.

PYTHON PROGRAM
Reg.No: 212222060229
Name: Sarvesan lathika

def addEdge(u, v):
	global adj
	adj[u].append(v)

def DFS(v):
	global visited, departure, time
	visited[v] = 1
	for i in adj[v]:
		if visited[i] == 0:
			DFS(i)
	departure[time] = v
	time += 1

def topologicalSort():
    for i in range(V):
        if visited[i]==0:
            DFS(i)
    for i in range(V-1, -1, -1):
        print(departure[i], end=" ")

if __name__ == '__main__':

	V,time, adj, visited, departure = 6, 0, [[] for i in range(7)], [0 for i in range(7)],[-1 for i in range(7)]
	addEdge(5, 2)
	addEdge(5, 0)
	addEdge(4, 0)
	addEdge(4, 1)
	addEdge(2, 3)
	addEdge(3, 1)

	print("Topological Sort of the given graph is")
	topologicalSort()
OUTPUT
image
RESULT
Hence, The program is successfully executed and the topological sorting of the given Directed Acyclic Graph (DAG) is verified.
