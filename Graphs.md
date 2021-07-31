# Graphs


**Graphs** -> A graph is a non-linear data structure that can be looked at as a collection of vertices  potentially connected by line segments named edges.

**common terminology of a graph:**
1. Vertex ->  A vertex, also called a node, is a data object that can have zero or more adjacent vertices.
2. Edge ->  An edge is a connection between two node.
3. Neighbor ->  The neighbors of a node are its adjacent nodes.
4. Degree ->  it is a vertex is the number of edges connected to that vertex.

**Complete vs Connected vs Disconnected Graphs:**
* Complete Graphs
A complete graph is when all nodes are connected .

* Connected
is a graph that has all of vertices,nodes have at least one edge.

* Disconnected
is a graph where some vertices may not had edges.

**Directed vs Undirected**

1.  Undirected Graphs((Bigraph))
is a graph where each edge is undirected or bi-directional. This means that the undirected graph doent move in any direction.

2.  directed Graphs((Digraph))
is a graph where every edge is directed. Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

**Acyclic vs Cyclic**

1.  Acyclic Graph
is a directed graph without cycles.


2. cycle is when a node can be traversed through and potentially end up back at itself.A directed acyclic graph is also called a DAG. 


3. Cyclic Graphs
is a graph that has cycles. A cycle is defined as a path of a positive length that starts and ends at the same vertex.



**Graph Representation**

* Adjacency Matrix:
  - An Adjacency matrix is represented through a 2-D array.
 If there are n vertices, then we are looking at an n x n Boolean matrix.
* Adjacency List
  - An adjacency list is the most common way to represent graph.



**Weighted Graphs**
is a graph with numbers assigned to its edges. These numbers are called weights. 



**Breadth First**

In a breadth first traversal, you are starting at a specific node. 
This node should be specified when calling the BreadthFirst() method.
The breadth-first traversal of a graph is like that of the tree,
the difference is the graphs can have cycles.
When a graph has cycles and we are trying to traverse, 
this leaves  possibility to be in an infinite ,which is bad. To prevent this,
we need to had some sort of flag that specifies if we have already visited that vertices. 
Upon each visit, 
we just set the “visited” flag from false to true.

![img](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/BreadthFirst.PNG)



```
ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    DECLARE visited <-- new Set()

    breadth.Enqueue(vertex)
    visited.Add(vertex)

    while (breadth is not empty)
        DECLARE front <-- breadth.Dequeue()
        nodes.Add(front)

        for each child in front.Children
            if(child is not visited)
                visited.Add(child)
                breadth.Enqueue(child)   

    return nodes;

```


**Depth First**

* In a depth first traversal, we approach it a bit different than the way we do when working with a depth first traversal of a tree.
 Similar to how the breadth-first uses a queue, we will use a Stack for our depth-first traversal.

![img](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/depthTrav5.PNG)



**The algorithm for a depth first traversal is as follows:**

1. Push root node to the stack

2. Start a while loop while the stack isnt empty

3. Peek at  top node in the stack

4. If top node has unvisited children, mark  top node as visited, and then Push any unvisited children back to the stack.

5. If  top node doent have any unvisited children, pop that node off the stack

6. repeat until the stack be empty.



**examples of graphs in use:**

1. GPS and Mapping

2. Driving Directions

3. Social Networks

4. Airline Traffic

5. Netflix uses graphs for suggestions of products



