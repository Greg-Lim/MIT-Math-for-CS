# Simple Graphs
Simple Graphs
: A simple graph G consist of a non-empty set V, called ***vertices*** (or nodes) of G and a set E of two element subset of V. The element of E are called ***edges*** of G.
G = (V, E)
V = {v~1~, v~2~, v~3~, ..., v~n~}
E = {{v~i~, v~j~}, ...}
- Simple graphs do not contain any self-loops. No edge {a, a}
- Simple graphs do not contain more than one edge between a pair of vertices. In other words do not contain multiedges or multiple edges
- Simple graphs do not contain directed edges (that is edges of the form (a, b) instead of {a, b})

Adjacent Vertices
: Two vertices are said to be adjacent if they are joined by an edge.

<!--*[adjacent]: Two vertices are said to be adjacent if they are joined by an edge.-->

Incident Edge
: An edge is said to be incident to the vertices it joins.

Degree of Vertex
:  The number of edges incident to a vertex v is called the degree of the vertex and is denoted by deg(v).
Equivalently, the degree of a vertex is equal to number vertices adjacent to it.

## Common graphs
Complete Graph
: The complete graph of n vertices, denoted by K~n~, has an edge between every two vertices for a total to $n(n-1)/2 edges.

Empty Graph
: The empty graph have vertices but not edges.

n-node Graph
: aka. Line graph
Denoted by L~n~
 L~n~ = (V, E) where
V = {v~1~, v~2~, ..., v~n~}
E = {{v~1~, v~2~}, {v~2~, v~3~}, ... {v~n-1~, v~n~}}

Simple Cycle Graph
: Denoted as C~n~
Is a line graph that has the added edge {v~n~, v~1~}


## Isomorphism
Two graph that look the same, have the same shape, might be different. A simple cycle graph with vertex set {a, b, c, d} and one with {1, 2, 3, 4} are not the same.

Isomorphism
: If G~1~ = {V~1~, E~1~}  and G~2~ = {V~2~, E~2~} are two graphs, then we say G~1~ is isomorphic to G~2~ iff there exist a bijection f : V~1~ → V~2~ such that for every pair of vertices u, v ∈ V~1~:
{u, v} ∈ E~1~ iff {f(u), f(v)} ∈ E~2~
The function f is called the isomorphism between G~1~ and G~2~.

A property of a graph is said to be preserved under isomorphism if whenever G has that property, every graph isomorphic to G also has that property.

## Subgraphs
Subgraphs
: A graph G~1~ = (V~1~, E~1~) is said to be a subgraph of graph G~2~ = (V~2~, E~2~) if V~1~ ⊆ V~2~ and E~1~ ⊆ E~2~.

## Weighted Graph
The edges of graph can be weighted.
This can be represented with an edge-weighted graph (weighted graph). 
A weighted graph is the same as a simple graph except its edges are associated with a real number.
A weighted graph consist of a graph G = (V, E) and a weight function w: E → R

## Adjacency Matrix
Like drawing a graph or using sets to represent a graph, adjacency matrix is another way to represent a graph

Adjacency Matrix
: Given an n-node graph G = (V, E) where V = {v~1~, v~2~, ..., v~n~},
the adjacentcy matrix for G is the n x n matrix G~g~ = {a~ij~} where
a~ij~ =
1 if {v~i~, v~j~}
0 otherwise

: If G is a weighted graph with edge weight given by w : E → R, then adjacency matrix for G is A~G~ = {a~ij~} where  
a~ij~ =
w({v~i~, v~j~}) if {v~i~, v~j~} ∈ E
0 otherwise

# Matching Problem

Handshaking Lemma
: The sum of the degrees of the vertices is a graph equals twice the number of edges.

### Bipartite Matchings
Bipartite Graph
: A bipartite graph is a graph together with a partition of its vertices into two sets, L and R, such that every edge is incident to a vertex in L and to a vertex in R.

### Matching Condition
- A ***matching*** in a graph, G is a set of edges such that no two edges in the set share a vertex.
- A matching is said to ***cover*** a set, L,  of vertices iff each vertex in L has an edge of the matching incident to it.
- A matching is said to be ***perfect*** if every node in the graph is incident to an edge in the matching.  
- In any graph, the set N(S), of the ***neighbor*** of some set, S, of vertices is the set of all vertices adjacent to some vertex in S. That is, $N(S) ::= \{r | \{s, r\} \text{ is an edge for some s ∈ S}\}$
The neighbor set is the set of all vertices that are adjacent to any element in a set
- S is called a ***bottleneck*** if $|S| > |N(S)|$

### Easy Matching Condition
Bipartite graph Degree-constrained
: A bipartite graph G with vertex partition L, R where |L| <= |R| is ***degree-constrained*** if deg(l) >= deg(r\) for every l ∈ L and r ∈ R.
All l in L at least n degree and all r in R at most n degree

Hall's Theorem
: Let G be a bipartite graph with vertex partition L, R where |L| ≤ |R|. If G is degree-constrained, then there is a matching that covers L.

Regular Graphs
: A graph is said to be ***regular*** if every node has the same degree.

## The Stable Marriage problem
For n men and n woman is there a way to match them such that all matches are stable where a match if stable if a men cannot find a women he prefers over his match and the women prefers him over her match.

### The Strategy
Using a *Mating Ritual*, each man and woman creates a list of partners they prefer arrange by preference. This strategy take place over a few days where each day they:
1. Morning each men propose to his most preferred women. 
2. Each women ask her most preferred men to propose to her tomorrow again and rejects the rest.
3. Any man that is rejected cross out that woman's name from his list

This daily pattern terminates when every women has a partner
- The procedure eventually Terminates
- Everybody ends up with someone
- The person they are with is stable

## Coloring
A Graph coloring problem is assigning a color to each vertices such that no two adjacent vertices have the same color.

Chromatic number
: The minimum value of k for which a graph G has a valid k-coloring is called its chromatic number, x(G).

### Degree-Bounded Coloring
It is quite hard to calculate the chromatic color of a graph but for some simple graph a lower and upper bound can be easily found
- If a graph is bipartite, then we can color it with 2 color
- If a graph is planer, like maps, then it is 4-colorable

# Walks
Walk
: A ***walk*** is a graph, G, is a sequence of 
 vertices: v~0~, v~1~, ..., v~k~
 and edges: {v~0~, v~1~}, {v~1~, v~2~}, ..., {v~k-1~, v~k~}
 such that {v~i~, v~i+1~} is an edge of G for all i where 0 ≤ i < k.
	 
- The walk is said to start at v~0~ and to end at v~k~ , and the ***length*** of the walk is defined to be k. 
- An edge, {u, v}, is ***traversed*** n times by the walk if there are n different values of i such that {v~i~, v~i+1~} = {u, v}.
- A ***path*** is a walk where all the vertices are different
- A ***closed walk*** is a walk that start and ends on the same vertex.
- A ***cycle*** is a walk v~0~, v~1~, ..., v~k-1~ are different vertices where k≥3.

If there is a walk from a vertex u to a vertex v in a graph, then there is a path from u to v.

Given a weighted graph, the length of a path in the graph is the sum of the weights of the edges in the path.

# Connectivity
- Two points are said to be ***connected*** if there is a path that begins from one point and ends at the other
- A graph is ***connected*** if every pair of vertices is connected.
- A ***connected component*** is a subgraph of a graph consisting of some vertex and every node and edge that is connected to that vertex.

### k-Connected Graphs
- Two vertices in a graph are ***k-edge connected*** if they remain connected in every subgraph obtained by deleting k - 1 edges.
- A graph with at least two vertices is ***k-edge connected*** if every two of its vertices are k-edge connecte

# Cycles and close walks
Closed walk
: A closed walk in a graph G is a sequence of vertices
v~0~, v~1~, ..., v~k~
and edges
{v~0~, v~1~}, {v~1~, v~2~}, ..., {v~k-1~, v~k~}
where v~0~ is the same node as v~k~ and {v~i~, v~i+1~} is an edge of G for all i where 0 ≤ i < k.
- The length of a closed walk is k.

Cycle
: A closed walk is said to be a cycle if k ≥ 3 and v~0~, ..., v~k~ are all different

Cycles are similar to path except paths have a starting and ending point but cycles starting and ending points don't matter

## Odd cycles and 2-colorability
The following properties of a graph are equivalent (that is, if the graph has any one of the property, then it has all the property.
	1. The graph is bipartite
	2. The graph is 2-colorable
	3. the graph does not contain any cycles with odd length
	4. The graph does not contain any closed walks with add length.

## Euler walk and euler tour 
Euler walk
: Euler walk is a path that travel each ***edge*** exactly once

Euler tour
: Euler tour is a Euler walk that start and end at the same vertices

A connected graph has an Euler tour iff every vertex has even degree.

## Hamiltonian Cycle
Hamiltonian Cycle
: A Hamiltonian Cycle in a graph G is a cycle that visits every ***node*** in G exactly once.

Hamiltonian Path
: A Hamiltonian path is a path that visits every ***node*** in G exactly once.

## The Traveling Salesperson Problem
Given a weighted graph, we want to find a Hamiltonian cycle that has least possible wight.

Given a weighted graph G, the ***weight*** of a cycle in G is defined as the sum of the weight s of the edges in the cycle

# Trees
Tree
: A graph with no cycles, an acyclic graph, is called a ***tree***.

Forest
: If every connected component in a graph G is a tree, then G is a forest.

Leaf
: A leaf is a node with degree 1 in a tree (or a forest)

A tree is usually drawn top down with the top node being the ***root*** and every edge joining a parent and child.
In the special case of ***ordered binary trees***, every node is the parent of at most 2 children and the children are labeled as being a left-child or a right-child.

## Properties of trees
Every tree have the following properties
1. Any connected subgraph is a tree
2. There is a unique simple path between every pair of vertices.
3. Adding an edge between nonadjacent nodes in a tree creates a graph with a cycle
4. Removing any edge disconnect the graph
5. If the tree has at least two vertices, then it has at least two leaves.
6. The number of vertices in a tree is one larger than the number of edges.

## Spanning trees
Spanning tree
: A spanning tree is a subgraph of a connected graph that has the same vertices as the graph.

Every connected graph contains a spanning tree.

## Minimum Weight Spanning Trees
Spanning trees are important because they connect every node of a graph with the smallest possible number of edges.
However in the real world there are often costs associated with the edges of the graph.
The ***weight*** of a spanning tree is the sum of weights of the edges in the tree.

Min-weight Spanning Tree
: The ***min-weight spanning tree*** (MST) of an edge-weighted graph G is the spanning tree of G with the smallest possible sum of edge weights.

### Algorithm to Find MST
Algorithm 1
: Grow a tree one edge at a time by adding the minimum weight edge possible to the tree, making sure that you have a tree at each step.

Algorithm 2
: Grow a subgraph one edge at a time by adding the minimum-weight edge possible to the subgraph, making sure that you have an acyclic subgraph at each step.

# Planner Graphs
A ***drawing of a graph in the plane*** consists of an assignment of vertices to distinct points in the plane and an assignment of edges to smooth, non-self-intersecting curves in the plane

The drawing is ***planer***, a ***planner drawing***, if none of the curves "cross"; That is, if the only points that appear on more than one curves are the vertex points.

A ***planner graph*** is a graph that has a planer drawing.

## Faces
In a planar drawing of a graph, the curves corresponding to the edges divide up the plane into ***connected regions***. These regions are called the ***continuous faces*** of the drawing. The vertices along the boundary of each of the faces form a cycle.

The face on the outside that stretch on to infinity is called the ***outside face***.

***bridge***
***dongle***

***Planar embedding***

## Euler formula
> If a connected graph has a planar embedding, then
> $$v - e + g = 2$$

	slkfjslkfj
		klsfksjflsfjslkf	
			skfjklsfjslfjslfksfslfskjfsjflsafjsfdfssssssssssssssssssssssssssssssss
