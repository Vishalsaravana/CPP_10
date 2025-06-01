# DEPTH FIRST SEARCH-DFS

## PROGRAM STATEMENT:

To write A C++ Program to implementation DFS using Vector STL

## ALGORITHM:  

1.	Start the program.
2.	Define graph structure: Create a 2D vector g to store the adjacency list and a vector v to track visited nodes.
3.	Edge addition: Define the addEdge function to add an undirected edge between nodes by updating the adjacency list.
4.	DFS visit: Implement the dfsVisit function to visit nodes recursively. Mark the node as visited and explore its neighbors.
5.	DFS traversal: Implement the dfs function, iterating over all nodes and calling dfsVisit for unvisited nodes to ensure the entire graph is explored.
6.	End the program: Input the number of nodes and edges from the user, then read and store the edges. Perform DFS and output the nodes in the order they are visited.
7.	End the program.

## PROGRAM:

```
#include <bits/stdc++.h> using namespace std; vector< vector <int>> g; vector<bool> v;
// Undirected graph
voidaddEdge(int a, int b)
{
g[a].push_back(b);
g[b].push_back(a);
}
voiddfsVisit(int u)
{
v[u] =true;
cout << u << " ";

for(auto i= g[u].begin(); i != g[u].end(); i++)
{
if(!v[*i])
dfsVisit(*i);
}
 
}
voiddfs(int n)
{
for(int u = 0; u < n; u++)
{
 
if(!v[u])

}
}
 

dfsVisit(u);
 
int main()
{
int n, e;
cin >> n >> e;

v.assign(n, false); g.assign(n, vector<int>());

int a, b;
for(int i= 0; i< e; i++)
{
 


}
dfs(n);
}
 
cin >> a >> b; addEdge(a, b);
 ```

## OUTPUT :
![image](https://github.com/user-attachments/assets/5c955b1c-0419-4655-bc1a-aeec84407668)

## RESULT:

Thus, the C++ program to write C++ Program to implementation DFS using Vector STL is created successfully.

