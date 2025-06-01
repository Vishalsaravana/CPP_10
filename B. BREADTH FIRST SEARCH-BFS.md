# BREADTH FIRST SEARCH-BFS
## PROGRAM STATEMENT:

To write A CPP Program to implement BFS using vectors and queue.

![image](https://github.com/user-attachments/assets/2e5017a1-0ec1-409b-8af9-84bf8fb3ce31)

## ALGORITHM:  

1.	Start the program.
2.	Define graph structure: Create a 2D vector g to store the adjacency list and a vector v to track visited nodes.
3.	Edge addition: Define the edge function to add an undirected edge between nodes by updating the adjacency list.
4.	BFS traversal: Implement BFS using a queue. Start from a node, mark it visited, and explore its neighbors in the queue.
5.	Input edges and nodes: Read the number of nodes and edges from the user, followed by pairs of nodes representing edges. Store these in the adjacency list.
6.	End the program: Traverse the graph, calling BFS on unvisited nodes, and output the BFS traversal order.

## PROGRAM:
```

// AQuick implementation ofBFS using
// vectors and queue #include <bits/stdc++.h> #define pb push_back using namespace std; vector<bool> v; vector<vector<char> > g; void edge(int a, int b)
{
g[a].pb(b);
}
 
void bfs(int u)
{
queue<char> q; q.push(u); v[u] =true;
while(!q.empty())
{
int f=q.front(); q.pop();
cout << f << " ";

for (auto i= g[f].begin(); i != g[f].end(); i++)
{
if (!v[*i])
{
q.push(*i); v[*i] =true;
}
}
}
}
int main()
{
int n, e;
cin >> n >> e;

v.assign(n, false); g.assign(n, vector<char>());

char a, b;
for (int i= 0; i< e; i++)
{
cin >> a >> b; edge(a, b);
}
for (int i= 0; i< n; i++)
{
 
if (!v[i])

}
 

bfs(i);
 
return 0;
}
 ```
## OUTPUT :
![image](https://github.com/user-attachments/assets/a3fefece-23a5-4737-9e53-cbc6020562e6)

## RESULT:

Thus, the C++ program to implement BFS using vectors and queue is created successfully

