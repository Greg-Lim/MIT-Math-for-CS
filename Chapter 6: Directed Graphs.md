---
extensions:
  markdown:
    # Disable "typographic replacements" such as (c), (tm), (p)
    typographer: false

---

<h1 id="directed-graphs">Directed Graphs</h1>
<h2 id="definations">Definations</h2>
<p>A directed edge is an edge where the end points are distinguished, one is the <em><strong>head</strong></em> and one is the <em><strong>tail</strong></em>.<br>
Directed edge is specified as an ordered pair of vertices u, v and is denoted by (u, v) or u → v, in this case u is the tail of the edge and v is the head.</p>
<dl>
<dt>Directed Graphs</dt>
<dd>A directed graph G = (V, E) consists of a nonempty set of nodes V and a set of directed edges E. Each edge e of E is specified by an ordered pair of vertices u, v ∈ V. A directed graph is a <em><strong>simple</strong></em> if it has no <em><strong>loops</strong></em> (edges of form u → u) and no multiple edges</dd>
</dl>
<p>Directed graphs are use when the relation is 1-way or asymmetric.</p>
<p>Directed graph have adjacency matrices just like undirected graphs</p>
<h3 id="degree">Degree</h3>
<p>In directed graphs, the notion of degree is split into <em><strong>indegree</strong></em> and <em><strong>outdegree</strong></em>.<br>
For example, for a graph with a node, c, that has 2 "arrows" in and 1 "arrow" out, the node will have indegree(c) = 2 and outdegree(c) = 1.<br>
If a node has outdegree 0, it is called a <em><strong>sink</strong></em>.<br>
If a node had indegree 0, it is called a <em><strong>source</strong></em>.</p>
<h3 id="walks-paths-and-cycles">Walks, Paths and Cycles</h3>
<p>Walks, paths and cycles in directed graphs are similar to undirected graphs except the direction of the edges need to be <em><strong>consistent</strong></em> with the order the walk is traversed</p>
<p>A directed <em><strong>walk</strong></em> (or more simply, a walk) in a directed graph G is a sequence of vertices v<sub>0</sub>, v<sub>1</sub>, . . . , v<sub>k</sub> and edges:<br>
v<sub>0</sub> → v<sub>1</sub>, v<sub>1</sub> → v<sub>2</sub>, . . . vk1 → v<sub>k</sub><br>
such that v<sub>i-1</sub> → v<sub>i</sub> is an edge of G for all i where 0 ≤ i &lt; k.</p>
<p>A directed <em><strong>path</strong></em> (or just path) in a directed graph is a walk where the nodes in the walk are all different.</p>
<p>A directed <em><strong>closed walk</strong></em> (or closed walk) in a directed graph is a walk where v<sub>0</sub> = v<sub>k</sub>.</p>
<p>A directed <em><strong>cycle</strong></em> (or cycle) in a directed graph is a closed walk where all the vertices v<sub>i</sub> are different for 0 ≤  i &lt; k.</p>
<p>A path or cycle in a directed graph is said to be <em><strong>Hamiltonian</strong></em> if it visits every node in the graph.</p>
<p>A walk in a directed graph is said to be <em><strong>Eulerian</strong></em> if it contains every edge.</p>
<h3 id="strong-connectivity">Strong connectivity</h3>
<p>A directed graph G = (V, E) is said to be <em><strong>strongly connected</strong></em> if for every pair of nodes, u, v ∈ V, there is  a directed path from u to v (and vice-versa) in G</p>
<p>A directed graph is said to be <em><strong>weakly connected</strong></em> (or, more simply, connected) if the corresponding undirected graph (where directed edges u → v and/or v → u are replaced with a single undirected edge {u, v} is connected.</p>
<h3 id="dags">DAGs</h3>
<p>A directed graph is called a <em><strong>directed acyclic graph</strong></em> (or, DAG) if it does not contain any directed cycles.<br>
Example to DAG graph:<br>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fe/Tred-G.svg/330px-Tred-G.svg.png" alt="Example of a directed acyclic graph"></p>
<h2 id="tournament-graphs">Tournament Graphs</h2>
<p>Suppose that n players compete in a round robin tournament such that every pair of players, u and v, compete and have only 1 winner, u or v. There might be many kinds of cycles such that a beats b and b beats c and c beats a.</p>
<p><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/89/4-tournament.svg/270px-4-tournament.svg.png" alt="Tournament Graph example"></p>
<p>The results of this tournament can be represented with a <em><strong>tournament graph</strong></em>.<br>
This is a directed graph<br>
Vertices represent players<br>
Edges indicate the outcomes of games<br>
An edge from u to v indicates that player u defeated player v<br>
Every pair of players have a match<br>
There is either an edge from u to v or v to u (but not both).</p>
<h3 id="finding-a-hamiltonian-path-in-a-tournament-graph">Finding a Hamiltonian Path in a Tournament Graph</h3>
<p>For every tournament, there exist a ranking of the players such that each player lost to the player 1 position higher.<br>
Proving such a ranking exist is amounts to proving that every tournament graph has a Hamiltonian path</p>
<h2 id="communication-networks">Communication Networks</h2>
<p>The goal of a communication network is to get data form <em><strong>inputs</strong></em> to <em><strong>outputs</strong></em>. This data can be in the form of packets.</p>
<h3 id="complete-binary-tree">Complete Binary Tree</h3>
<h3 id="network-diameter">Network diameter</h3>
<p>The longest of the shortest routes between all inputs and outputs is the <em><strong>diameter</strong></em> of the network</p>
<p>The diameter of a complete binary tree with N inputs and outputs is 2 log<sub>2</sub> N + 2.</p>
<h3 id="switch-size">Switch Size</h3>
<p>The diameter of a network can be improve by increasing the switch size in the network. A 2 x 2 switch will have 2 inputs and 2 outputs. But a 3 x 3 switch or 4 x 4 switch can reduce the diameter of a network.<br>
A N x N switch will have a latency of 2.</p>
<h3 id="switch-count">Switch Count</h3>
<p>Another goal in designing a network is to use as few switches as possible.<br>
The number of switches in a complete binary tree is 2N - 1.</p>
<h3 id="congestion">Congestion</h3>
<p>A complete binary tree has a bottle neck as every packet traveling from the left side of the tree to the right side goes through the root switch.</p>
<p>If one of switch fails, the network will be split in to 2 parts.</p>
<p>We can distinguish between a “good” set of paths and a “bad” set based on congestion. The <em><strong>congestion</strong></em> of a routing, P, is equal to the largest number of paths in P that pass through a single switch.</p>
<p>We can also distinguish between “good” and “bad” networks with respect to bottleneck problems. For each routing problem, π, for the network, we assume a routing is chosen that optimizes congestion, that is, that has the minimum congestion among all routings that solve π. Then the largest congestion that will ever be suffered by a switch will be the maximum congestion among these optimal routings. This “maxi-min” congestion is called the <em><strong>congestion of the network</strong></em>.</p>
<p>A complete binary tree does well in low number of switches and low switch complexity but does terrible in congestion</p>
<h3 id="the-2-d-array">The 2-d Array</h3>
<p><img src="https://i.imgur.com/lwcWqfk.png" alt="check if this image disappears"><br>
The congestion of an N-input 2-d array is 2<br>
However the grid method has a major drawback of having N<sup>2</sup> switches</p>
<h3 id="the-butterfly">The Butterfly</h3>
<p>The ideal switching network would combine the best properties of the complete binary tree (low diameter, few switches) and the array (low congestion).<br>
The <em><strong>Butterfly</strong></em> is a widely use compromise between the two.<br>
<img src="https://i.imgur.com/eLYcY5r.png" alt="An 8-input/output butterfly"></p>
<h3 id="benes-network">Benes Network</h3>
<p>A network with 2 butterfly network attached to each other.<br>
<img src="https://i.imgur.com/AyLe8ic.png" alt="Benes Network"></p>

