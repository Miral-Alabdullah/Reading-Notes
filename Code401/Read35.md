# Graph

A graph is a non-linear data structure that can be looked at as a collection of `vertices` (or `nodes`) potentially connected by line segments named `edges`.

- Common terminology used when working with Graphs:

1- `Vertex` - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.

2- `Edge` - An edge is a connection between two nodes.

3- `Neighbor` - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.

4- `Degree` - The degree of a vertex is the number of edges connected to that vertex.


![graph](https://lh3.googleusercontent.com/proxy/U-I0l4F0V46Lyr7Y9OLku1XHiEkOJOC5zGJW0-ubrdh2D8hXg86qo8WanX48qQ5fzTnXnzAJaavmOva5f1yXHRQP8ijoQGn1KSlYqha7aTDWOsorQJaOTAvRAHotfg)

<br>

# Directed vs Undirected


## Undirected Graphs

- An `Undirected Graph` is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

![undirect](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/UndirectedGraph.PNG)

```
Vertices/Nodes = {a,b,c,d,e,f}

Edges = {(a,c),(a,d),(b,c),(b,f),(c,e),(d,e),(e,f)}
```

<br>
<br>

## Directed Graphs (Digraph)

- A `Directed Graph` also called a `Digraph` is a graph where every edge is directed.

![direct](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DirectedGraph.PNG)

```
Vertices = {a,b,c,d,e,f}

Edges = {(a,c),(b,c),(b,f),(c,e),(d,a),(d,e)(e,c)(e,f)}
```

<br>
<br>


# Complete vs Connected vs Disconnected

 * Complete Graphs

   - A complete graph is when all nodes are connected to all other nodes.

 * Connected Graphs

   - A connected graph is graph that has all of vertices/nodes have at least one edge.

 * Disconnected Graphs

   - A disconnected graph is a graph where some vertices may not have edges.

<br>
<br>

# Acyclic vs Cyclic

 ## Acyclic Graph

   - An acyclic graph is a directed graph without cycles.

   - When a node can be traversed through and potentially end up back at itself.

 ## Cyclic Graphs

   - A Cyclic graph is a graph that has cycles.

   - A path of a positive length that starts and ends at the same vertex.


<br>
<br>

# Graph Representation

  * Adjacency Matrix.
  
  * Adjacency List.

