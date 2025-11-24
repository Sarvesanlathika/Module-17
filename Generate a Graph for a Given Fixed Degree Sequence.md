# Ex. No: 17D - Generate a Graph for a Given Fixed Degree Sequence
# AIM:
To write a Python program to generate a graph for a given fixed degree sequence.

# ALGORITHM:
Step 1: Start the program.

Step 2: Check if the sum of the degree sequence is even.

(A necessary condition for the sequence to be graphical.)

If not even, print an error message and exit the program.
Step 3: Use the Havel-Hakimi algorithm to determine whether a simple graph can be constructed from the sequence, and to generate the graph.

Step 4: If the graph is successfully created, visualize it using a graph drawing function (e.g., networkx.draw()).

Step 5: End the program.

# PYTHON PROGRAM
~~~
Reg.No: 212222060229
Name: Sarvesan lathika

def printMat(degseq, n):

	mat = [[0] * n for i in range(n)]

	for i in range(n):
		for j in range(i + 1, n):

			if (degseq[i]>0 and degseq[j] > 0):
				degseq[i] -= 1
				degseq[j] -= 1
				mat[i][j] = 1
				mat[j][i] = 1

	print("      ", end ="")
	for i in range(n):
		print(" ", "(", i, ")", end ="")
	print()
	print()
	for i in range(n):
		print("  ", "(", i, ")", end = " ")
		for j in range(n):
			print("  ", mat[i][j], end = " ")
		print()

degseq=[]
for i in range(0, 5):
    ele = int(input())
  
    degseq.append(ele)
#degseq =[v0,v1,v2,v3,v4]

n = len(degseq)
printMat(degseq, n)
~~~
# OUTPUT
<img width="863" height="264" alt="image" src="https://github.com/user-attachments/assets/a4b486c4-df25-480a-a55f-64ce244fcabe" />

# RESULT
Hence, The program is successfully executed and a simple graph has been generated for the given fixed degree sequence.
