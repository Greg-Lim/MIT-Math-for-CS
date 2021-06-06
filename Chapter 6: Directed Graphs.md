# Directed Graphs
## Definations
A directed edge is an edge where the end points are distinguished, one is the ***head*** and one is the ***tail***. 
Directed edge is specified as an ordered pair of vertices u, v and is denoted by (u, v) or u → v, in this case u is the tail of the edge and v is the head.

Directed Graphs
: A directed graph G = (V, E) consists of a nonempty set of nodes V and a set of directed edges E. Each edge e of E is specified by an ordered pair of vertices u, v ∈ V. A directed graph is a ***simple*** if it has no ***loops*** (edges of form u → u) and no multiple edges

Directed graphs are use when the relation is 1-way or asymmetric.

Directed graph have adjacency matrices just like undirected graphs

### Degree
In directed graphs, the notion of degree is split into ***indegree*** and ***outdegree***.
For example, for a graph with a node, c, that has 2 "arrows" in and 1 "arrow" out, the node will have indegree(c) = 2 and outdegree(c) = 1.
If a node has outdegree 0, it is called a ***sink***.
If a node had indegree 0, it is called a ***source***.

###  Walks, Paths and Cycles
Walks, paths and cycles in directed graphs are similar to undirected graphs except the direction of the edges need to be ***consistent*** with the order the walk is traversed

A directed ***walk*** (or more simply, a walk) in a directed graph G is a sequence of vertices v~0~, v~1~, . . . , v~k~ and edges:
v~0~ → v~1~, v~1~ → v~2~, . . . vk1 → v~k~
such that v~i-1~ → v~i~ is an edge of G for all i where 0 ≤ i < k.

A directed ***path*** (or just path) in a directed graph is a walk where the nodes in the walk are all different.

A directed ***closed walk*** (or closed walk) in a directed graph is a walk where v~0~ = v~k~.

A directed ***cycle*** (or cycle) in a directed graph is a closed walk where all the vertices v~i~ are different for 0 ≤  i < k.

A path or cycle in a directed graph is said to be ***Hamiltonian*** if it visits every node in the graph.

A walk in a directed graph is said to be ***Eulerian*** if it contains every edge.

### Strong connectivity
A directed graph G = (V, E) is said to be ***strongly connected*** if for every pair of nodes, u, v ∈ V, there is  a directed path from u to v (and vice-versa) in G

A directed graph is said to be ***weakly connected*** (or, more simply, connected) if the corresponding undirected graph (where directed edges u → v and/or v → u are replaced with a single undirected edge {u, v} is connected.

### DAGs
A directed graph is called a ***directed acyclic graph*** (or, DAG) if it does not contain any directed cycles.
Example to DAG graph:
![Example of a directed acyclic graph](https://upload.wikimedia.org/wikipedia/commons/thumb/f/fe/Tred-G.svg/330px-Tred-G.svg.png)


## Tournament Graphs
Suppose that n players compete in a round robin tournament such that every pair of players, u and v, compete and have only 1 winner, u or v. There might be many kinds of cycles such that a beats b and b beats c and c beats a.
![Tournament Graph example](https://upload.wikimedia.org/wikipedia/commons/thumb/8/89/4-tournament.svg/270px-4-tournament.svg.png)

The results of this tournament can be represented with a ***tournament graph***.
This is a directed graph
Vertices represent players
Edges indicate the outcomes of games
An edge from u to v indicates that player u defeated player v
Every pair of players have a match
There is either an edge from u to v or v to u (but not both).

### Finding a Hamiltonian Path in a Tournament Graph
For every tournament, there exist a ranking of the players such that each player lost to the player 1 position higher.
Proving such a ranking exist is amounts to proving that every tournament graph has a Hamiltonian path

## Communication Networks
The goal of a communication network is to get data form ***inputs*** to ***outputs***. This data can be in the form of packets.
### Complete Binary Tree

### Network diameter
The longest of the shortest routes between all inputs and outputs is the ***diameter*** of the network

The diameter of a complete binary tree with N inputs and outputs is 2 log~2~ N + 2.

### Switch Size
The diameter of a network can be improve by increasing the switch size in the network. A 2 x 2 switch will have 2 inputs and 2 outputs. But a 3 x 3 switch or 4 x 4 switch can reduce the diameter of a network.
A N x N switch will have a latency of 2.

### Switch Count
Another goal in designing a network is to use as few switches as possible.
The number of switches in a complete binary tree is 2N - 1.

### Congestion
A complete binary tree has a bottle neck as every packet traveling from the left side of the tree to the right side goes through the root switch.

If one of switch fails, the network will be split in to 2 parts.

We can distinguish between a “good” set of paths and a “bad” set based on congestion. The ***congestion*** of a routing, P, is equal to the largest number of paths in P that pass through a single switch.

We can also distinguish between “good” and “bad” networks with respect to bottleneck problems. For each routing problem, π, for the network, we assume a routing is chosen that optimizes congestion, that is, that has the minimum congestion among all routings that solve π. Then the largest congestion that will ever be suffered by a switch will be the maximum congestion among these optimal routings. This “maxi-min” congestion is called the ***congestion of the network***.

A complete binary tree does well in low number of switches and low switch complexity but does terrible in congestion

### The 2-d Array
![check if this image disappears](https://i.imgur.com/lwcWqfk.png)
The congestion of an N-input 2-d array is 2
However the grid method has a major drawback of having N^2^ switches

### The Butterfly
The ideal switching network would combine the best properties of the complete binary tree (low diameter, few switches) and the array (low congestion).
The ***Butterfly*** is a widely use compromise between the two.
![An 8-input/output butterfly](https://i.imgur.com/eLYcY5r.png)

### Benes Network
A network with 2 butterfly network attached to each other.
Benes Network has a congestion of 1.
![Benes Network](https://i.imgur.com/AyLe8ic.png)


