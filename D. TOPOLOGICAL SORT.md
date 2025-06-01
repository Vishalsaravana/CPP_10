# TOPOLOGICAL SORT
## PROGRAM STATEMENT:

To write A C++ Program for Topological Sorting

## ALGORITHM:  

1.	Initialize the graph with vertices and edges.
2.	Add edges to the adjacency list.
3.	Create a visited array and iterate over all vertices.
4.	Use DFS to recursively explore unvisited vertices.
5.	Push each vertex to the stack after processing its neighbors.
6.	Pop and print vertices from the stack to get the topological order.

## PROGRAM:

```
#include <iostream> #include <list> #include <stack> usingnamespacestd; class Graph
{
int V; list<int>* adj;
void topologicalSortUtil(int v, boolvisited[], stack<int>& Stack); public:
Graph(int V); // Constructor

voidaddEdge(int v, int w); // function to add an edge to graph

voidtopologicalSort();// printsa Topological Sort ofthe completegraph
};
Graph::Graph(int V)
{
this->V = V;
adj= new list<int>[V];
}
void Graph::addEdge(int v, int w)
{
adj[v].push_back(w); // Addw to v’s list.
}
// Arecursive functionused bytopologicalSort
 
void Graph::topologicalSortUtil(int v, boolvisited[], stack<int>& Stack)
{
visited[v] =true;// Markthecurrent node as visited. list<int>::iterator i;
for (i= adj[v].begin(); i != adj[v].end(); ++i) if (!visited[*i])
topologicalSortUtil(*i, visited, Stack);

Stack.push(v);
}
void Graph::topologicalSort()
{
stack<int> Stack;
bool* visited=newbool[V]; for (int i= 0; i< V; i++)
visited[i] = false;

for (int i= 0; i< V; i++)
if(visited[i] == false)
topologicalSortUtil(i, visited, Stack);

while (Stack.empty() == false)
{
cout << Stack.top() << ""; Stack.pop();
}
}
int main()
{
int a,b,n;
cin>>n; Graphg(n);
for(int i=0;i<6;i++)
{
cin>>a>>b; g.addEdge(a, b);
}
cout << "Topological Sort ofthe givengraphn"<<endl; g.topologicalSort();
return 0;
}
 ```
## OUTPUT :
![image](https://github.com/user-attachments/assets/20a0c95e-36b9-4ac2-b43b-49c35f8a988d)

## RESULT:

Thus, the C++ program for Topological Sorting STL is created successfully.
 


