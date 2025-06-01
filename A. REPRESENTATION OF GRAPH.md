# D. TOPOLOGICAL SORT 
## PROGRAM STATEMENT:

To write A C++ Program to represent the Adjacency Matrix.

![image](https://github.com/user-attachments/assets/ea0dd56c-3dbf-4d8e-ad77-86eb149e2740)

## ALGORITHM:  

1.	Start the program.
2.	Define a graph matrix: Create a 2D array vertArr to represent the graph, initialized to 0.
3.	Add edges: The add_edge function sets the corresponding matrix entries to 1 for both directions (undirected graph).
4.	Input edges: Use a loop to take 6 pairs of inputs representing edges.
5.	Display adjacency matrix: The displayMatrix function prints the adjacency matrix, showing connections between vertices.
6.	End the program.

## PROGRAM:

```
#include<iostream> usingnamespacestd; int vertArr[20][20]; int count = 0;
voiddisplayMatrix(int v)
{
int i, j;
for(i = 0; i< v; i++)
{
for(j = 0; j< v; j++)
{
cout << vertArr[i][j] << " ";
}
 
cout << endl;
}
}
void add_edge(int u, int v)
{
vertArr[u][v] = 1;
vertArr[v][u] = 1;
}
int main()
{
int v= 6,a,b; //there are 6 vertices in thegraph for(int i=0;i<6;i++)
{
cin>>a>>b; add_edge(a, b);
}
displayMatrix(v); return 0;
}
 ```
## OUTPUT :
![image](https://github.com/user-attachments/assets/49cebf19-db7d-44e5-97d3-b8625560de08)

## RESULT:

Thus, the C++ program to represent the Adjacency Matrix is created successfully.
 

