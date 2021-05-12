<h1 id="simple-graphs">Simple Graphs</h1>
<dl>
<dt>Simple Graphs</dt>
<dd>A simple graph G consist of a non-empty set V, called <em><strong>vertices</strong></em> (or nodes) of G and a set E of two element subset of V. The element of E are called <em><strong>edges</strong></em> of G.<br>
G = (V, E)<br>
V = {v<sub>1</sub>, v<sub>2</sub>, v<sub>3</sub>, …, v<sub>n</sub>}<br>
E = {{v<sub>i</sub>, v<sub>j</sub>}, …}</dd>
</dl>
<ul>
<li>Simple graphs do not contain any self-loops. No edge {a, a}</li>
<li>Simple graphs do not contain more than one edge between a pair of vertices. In other words do not contain multiedges or multiple edges</li>
<li>Simple graphs do not contain directed edges (that is edges of the form (a, b) instead of {a, b})</li>
</ul>
<dl>
<dt>Adjacent Vertices</dt>
<dd>Two vertices are said to be adjacent if they are joined by an edge.</dd>
</dl>
<!--*[adjacent]: Two vertices are said to be adjacent if they are joined by an edge.-->
<dl>
<dt>Incident Edge</dt>
<dd>An edge is said to be incident to the vertices it joins.</dd>
<dt>Degree of Vertex</dt>
<dd>The number of edges incident to a vertex v is called the degree of the vertex and is denoted by deg(v).<br>
Equivalently, the degree of a vertex is equal to number vertices adjacent to it.</dd>
</dl>
<h2 id="common-graphs">Common graphs</h2>
<dl>
<dt>Complete Graph</dt>
<dd>The complete graph of n vertices, denoted by K<sub>n</sub>, has an edge between every two vertices for a total to $n(n-1)/2 edges.</dd>
<dt>Empty Graph</dt>
<dd>The empty graph have vertices but not edges.</dd>
<dt>n-node Graph</dt>
<dd>aka. Line graph<br>
Denoted by L<sub>n</sub><br>
L<sub>n</sub> = (V, E) where<br>
V = {v<sub>1</sub>, v<sub>2</sub>, …, v<sub>n</sub>}<br>
E = {{v<sub>1</sub>, v<sub>2</sub>}, {v<sub>2</sub>, v<sub>3</sub>}, … {v<sub>n-1</sub>, v<sub>n</sub>}}</dd>
<dt>Simple Cycle Graph</dt>
<dd>Denoted as C<sub>n</sub><br>
Is a line graph that has the added edge {v<sub>n</sub>, v<sub>1</sub>}</dd>
</dl>
<h2 id="isomorphism">Isomorphism</h2>
<p>Two graph that look the same, have the same shape, might be different. A simple cycle graph with vertex set {a, b, c, d} and one with {1, 2, 3, 4} are not the same.</p>
<dl>
<dt>Isomorphism</dt>
<dd>If G<sub>1</sub> = {V<sub>1</sub>, E<sub>1</sub>}  and G<sub>2</sub> = {V<sub>2</sub>, E<sub>2</sub>} are two graphs, then we say G<sub>1</sub> is isomorphic to G<sub>2</sub> iff there exist a bijection f : V<sub>1</sub> → V<sub>2</sub> such that for every pair of vertices u, v ∈ V<sub>1</sub>:<br>
{u, v} ∈ E<sub>1</sub> iff {f(u), f(v)} ∈ E<sub>2</sub><br>
The function f is called the isomorphism between G<sub>1</sub> and G<sub>2</sub>.</dd>
</dl>
<p>A property of a graph is said to be preserved under isomorphism if whenever G has that property, every graph isomorphic to G also has that property.</p>
<h2 id="subgraphs">Subgraphs</h2>
<dl>
<dt>Subgraphs</dt>
<dd>A graph G<sub>1</sub> = (V<sub>1</sub>, E<sub>1</sub>) is said to be a subgraph of graph G<sub>2</sub> = (V<sub>2</sub>, E<sub>2</sub>) if V<sub>1</sub> ⊆ V<sub>2</sub> and E<sub>1</sub> ⊆ E<sub>2</sub>.</dd>
</dl>
<h2 id="weighted-graph">Weighted Graph</h2>
<p>The edges of graph can be weighted.<br>
This can be represented with an edge-weighted graph (weighted graph).<br>
A weighted graph is the same as a simple graph except its edges are associated with a real number.<br>
A weighted graph consist of a graph G = (V, E) and a weight function w: E → R</p>
<h2 id="adjacency-matrix">Adjacency Matrix</h2>
<p>Like drawing a graph or using sets to represent a graph, adjacency matrix is another way to represent a graph</p>
<dl>
<dt>Adjacency Matrix</dt>
<dd>
<p>Given an n-node graph G = (V, E) where V = {v<sub>1</sub>, v<sub>2</sub>, …, v<sub>n</sub>},<br>
the adjacentcy matrix for G is the n x n matrix G<sub>g</sub> = {a<sub>ij</sub>} where<br>
a<sub>ij</sub> =<br>
1 if {v<sub>i</sub>, v<sub>j</sub>}<br>
0 otherwise</p>
</dd>
<dd>
<p>If G is a weighted graph with edge weight given by w : E → R, then adjacency matrix for G is A<sub>G</sub> = {a<sub>ij</sub>} where<br>
a<sub>ij</sub> =<br>
w({v<sub>i</sub>, v<sub>j</sub>}) if {v<sub>i</sub>, v<sub>j</sub>} ∈ E<br>
0 otherwise</p>
</dd>
</dl>
<h1 id="matching-problem">Matching Problem</h1>
<dl>
<dt>Handshaking Lemma</dt>
<dd>The sum of the degrees of the vertices is a graph equals twice the number of edges.</dd>
</dl>
<h3 id="bipartite-matchings">Bipartite Matchings</h3>
<dl>
<dt>Bipartite Graph</dt>
<dd>A bipartite graph is a graph together with a partition of its vertices into two sets, L and R, such that every edge is incident to a vertex in L and to a vertex in R.</dd>
</dl>
<h3 id="matching-condition">Matching Condition</h3>
<ul>
<li>A <em><strong>matching</strong></em> in a graph, G is a set of edges such that no two edges in the set share a vertex.</li>
<li>A matching is said to <em><strong>cover</strong></em> a set, L,  of vertices iff each vertex in L has an edge of the matching incident to it.</li>
<li>A matching is said to be <em><strong>perfect</strong></em> if every node in the graph is incident to an edge in the matching.</li>
<li>In any graph, the set N(S), of the <em><strong>neighbor</strong></em> of some set, S, of vertices is the set of all vertices adjacent to some vertex in S. That is, <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>N</mi><mo stretchy="false">(</mo><mi>S</mi><mo stretchy="false">)</mo><mo>:</mo><mo>:</mo><mo>=</mo><mo stretchy="false">{</mo><mi>r</mi><mi mathvariant="normal">∣</mi><mo stretchy="false">{</mo><mi>s</mi><mo separator="true">,</mo><mi>r</mi><mo stretchy="false">}</mo><mtext>&nbsp;is&nbsp;an&nbsp;edge&nbsp;for&nbsp;some&nbsp;s&nbsp;∈&nbsp;S</mtext><mo stretchy="false">}</mo></mrow><annotation encoding="application/x-tex">N(S) ::= \{r | \{s, r\} \text{ is an edge for some s ∈ S}\}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mord mathnormal" style="margin-right: 0.10903em;">N</span><span class="mopen">(</span><span class="mord mathnormal" style="margin-right: 0.05764em;">S</span><span class="mclose">)</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">::=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mopen">{</span><span class="mord mathnormal" style="margin-right: 0.02778em;">r</span><span class="mord">∣</span><span class="mopen">{</span><span class="mord mathnormal">s</span><span class="mpunct">,</span><span class="mspace" style="margin-right: 0.166667em;"></span><span class="mord mathnormal" style="margin-right: 0.02778em;">r</span><span class="mclose">}</span><span class="mord text"><span class="mord">&nbsp;is&nbsp;an&nbsp;edge&nbsp;for&nbsp;some&nbsp;s&nbsp;∈&nbsp;S</span></span><span class="mclose">}</span></span></span></span></span><br>
The neighbor set is the set of all vertices that are adjacent to any element in a set</li>
<li>S is called a <em><strong>bottleneck</strong></em> if <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi mathvariant="normal">∣</mi><mi>S</mi><mi mathvariant="normal">∣</mi><mo>&gt;</mo><mi mathvariant="normal">∣</mi><mi>N</mi><mo stretchy="false">(</mo><mi>S</mi><mo stretchy="false">)</mo><mi mathvariant="normal">∣</mi></mrow><annotation encoding="application/x-tex">|S| &gt; |N(S)|</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mord">∣</span><span class="mord mathnormal" style="margin-right: 0.05764em;">S</span><span class="mord">∣</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">&gt;</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 1em; vertical-align: -0.25em;"></span><span class="mord">∣</span><span class="mord mathnormal" style="margin-right: 0.10903em;">N</span><span class="mopen">(</span><span class="mord mathnormal" style="margin-right: 0.05764em;">S</span><span class="mclose">)</span><span class="mord">∣</span></span></span></span></span></li>
</ul>
<h3 id="easy-matching-condition">Easy Matching Condition</h3>
<dl>
<dt>Bipartite graph Degree-constrained</dt>
<dd>A bipartite graph G with vertex partition L, R where |L| &lt;= |R| is <em><strong>degree-constrained</strong></em> if deg(l) &gt;= deg(r) for every l ∈ L and r ∈ R.<br>
All l in L at least n degree and all r in R at most n degree</dd>
<dt>Hall’s Theorem</dt>
<dd>Let G be a bipartite graph with vertex partition L, R where |L| ≤ |R|. If G is degree-constrained, then there is a matching that covers L.</dd>
<dt>Regular Graphs</dt>
<dd>A graph is said to be <em><strong>regular</strong></em> if every node has the same degree.</dd>
</dl>
<h2 id="the-stable-marriage-problem">The Stable Marriage problem</h2>
<p>For n men and n woman is there a way to match them such that all matches are stable where a match if stable if a men cannot find a women he prefers over his match and the women prefers him over her match.</p>
<h3 id="the-strategy">The Strategy</h3>
<p>Using a <em>Mating Ritual</em>, each man and woman creates a list of partners they prefer arrange by preference. This strategy take place over a few days where each day they:</p>
<ol>
<li>Morning each men propose to his most preferred women.</li>
<li>Each women ask her most preferred men to propose to her tomorrow again and rejects the rest.</li>
<li>Any man that is rejected cross out that woman’s name from his list</li>
</ol>
<p>This daily pattern terminates when every women has a partner</p>
<ul>
<li>The procedure eventually Terminates</li>
<li>Everybody ends up with someone</li>
<li>The person they are with is stable</li>
</ul>
<h2 id="coloring">Coloring</h2>
<p>A Graph coloring problem is assigning a color to each vertices such that no two adjacent vertices have the same color.</p>
<dl>
<dt>Chromatic number</dt>
<dd>The minimum value of k for which a graph G has a valid k-coloring is called its chromatic number, x(G).</dd>
</dl>
<h3 id="degree-bounded-coloring">Degree-Bounded Coloring</h3>
<p>It is quite hard to calculate the chromatic color of a graph but for some simple graph a lower and upper bound can be easily found</p>
<ul>
<li>If a graph is bipartite, then we can color it with 2 color</li>
<li>If a graph is planer, like maps, then it is 4-colorable</li>
</ul>
<h1 id="walks">Walks</h1>
<dl>
<dt>Walk</dt>
<dd>A <em><strong>walk</strong></em> is a graph, G, is a sequence of<br>
vertices: v<sub>0</sub>, v<sub>1</sub>, …, v<sub>k</sub><br>
and edges: {v<sub>0</sub>, v<sub>1</sub>}, {v<sub>1</sub>, v<sub>2</sub>}, …, {v<sub>k-1</sub>, v<sub>k</sub>}<br>
such that {v<sub>i</sub>, v<sub>i+1</sub>} is an edge of G for all i where 0 ≤ i &lt; k.</dd>
</dl>
<ul>
<li>The walk is said to start at v<sub>0</sub> and to end at v<sub>k</sub> , and the <em><strong>length</strong></em> of the walk is defined to be k.</li>
<li>An edge, {u, v}, is <em><strong>traversed</strong></em> n times by the walk if there are n different values of i such that {v<sub>i</sub>, v<sub>i+1</sub>} = {u, v}.</li>
<li>A <em><strong>path</strong></em> is a walk where all the vertices are different</li>
<li>A <em><strong>closed walk</strong></em> is a walk that start and ends on the same vertex.</li>
<li>A <em><strong>cycle</strong></em> is a walk v<sub>0</sub>, v<sub>1</sub>, …, v<sub>k-1</sub> are different vertices where k≥3.</li>
</ul>
<p>If there is a walk from a vertex u to a vertex v in a graph, then there is a path from u to v.</p>
<p>Given a weighted graph, the length of a path in the graph is the sum of the weights of the edges in the path.</p>
<h1 id="connectivity">Connectivity</h1>
<ul>
<li>Two points are said to be <em><strong>connected</strong></em> if there is a path that begins from one point and ends at the other</li>
<li>A graph is <em><strong>connected</strong></em> if every pair of vertices is connected.</li>
<li>A <em><strong>connected component</strong></em> is a subgraph of a graph consisting of some vertex and every node and edge that is connected to that vertex.</li>
</ul>
<h3 id="k-connected-graphs">k-Connected Graphs</h3>
<ul>
<li>Two vertices in a graph are <em><strong>k-edge connected</strong></em> if they remain connected in every subgraph obtained by deleting k - 1 edges.</li>
<li>A graph with at least two vertices is <em><strong>k-edge connected</strong></em> if every two of its vertices are k-edge connecte</li>
</ul>
<h1 id="cycles-and-close-walks">Cycles and close walks</h1>
<dl>
<dt>Closed walk</dt>
<dd>A closed walk in a graph G is a sequence of vertices<br>
v<sub>0</sub>, v<sub>1</sub>, …, v<sub>k</sub><br>
and edges<br>
{v<sub>0</sub>, v<sub>1</sub>}, {v<sub>1</sub>, v<sub>2</sub>}, …, {v<sub>k-1</sub>, v<sub>k</sub>}<br>
where v<sub>0</sub> is the same node as v<sub>k</sub> and {v<sub>i</sub>, v<sub>i+1</sub>} is an edge of G for all i where 0 ≤ i &lt; k.</dd>
</dl>
<ul>
<li>The length of a closed walk is k.</li>
</ul>
<dl>
<dt>Cycle</dt>
<dd>A closed walk is said to be a cycle if k ≥ 3 and v<sub>0</sub>, …, v<sub>k</sub> are all different</dd>
</dl>
<p>Cycles are similar to path except paths have a starting and ending point but cycles starting and ending points don’t matter</p>
<h2 id="odd-cycles-and-2-colorability">Odd cycles and 2-colorability</h2>
<p>The following properties of a graph are equivalent (that is, if the graph has any one of the property, then it has all the property.<br>
1. The graph is bipartite<br>
2. The graph is 2-colorable<br>
3. the graph does not contain any cycles with odd length<br>
4. The graph does not contain any closed walks with add length.</p>
<h2 id="euler-walk-and-euler-tour">Euler walk and euler tour</h2>
<dl>
<dt>Euler walk</dt>
<dd>Euler walk is a path that travel each <em><strong>edge</strong></em> exactly once</dd>
<dt>Euler tour</dt>
<dd>Euler tour is a Euler walk that start and end at the same vertices</dd>
</dl>
<p>A connected graph has an Euler tour iff every vertex has even degree.</p>
<h2 id="hamiltonian-cycle">Hamiltonian Cycle</h2>
<dl>
<dt>Hamiltonian Cycle</dt>
<dd>A Hamiltonian Cycle in a graph G is a cycle that visits every <em><strong>node</strong></em> in G exactly once.</dd>
<dt>Hamiltonian Path</dt>
<dd>A Hamiltonian path is a path that visits every <em><strong>node</strong></em> in G exactly once.</dd>
</dl>
<h2 id="the-traveling-salesperson-problem">The Traveling Salesperson Problem</h2>
<p>Given a weighted graph, we want to find a Hamiltonian cycle that has least possible wight.</p>
<p>Given a weighted graph G, the <em><strong>weight</strong></em> of a cycle in G is defined as the sum of the weight s of the edges in the cycle</p>
<h1 id="trees">Trees</h1>
<dl>
<dt>Tree</dt>
<dd>A graph with no cycles, an acyclic graph, is called a <em><strong>tree</strong></em>.</dd>
<dt>Forest</dt>
<dd>If every connected component in a graph G is a tree, then G is a forest.</dd>
<dt>Leaf</dt>
<dd>A leaf is a node with degree 1 in a tree (or a forest)</dd>
</dl>
<p>A tree is usually drawn top down with the top node being the <em><strong>root</strong></em> and every edge joining a parent and child.<br>
In the special case of <em><strong>ordered binary trees</strong></em>, every node is the parent of at most 2 children and the children are labeled as being a left-child or a right-child.</p>
<h2 id="properties-of-trees">Properties of trees</h2>
<p>Every tree have the following properties</p>
<ol>
<li>Any connected subgraph is a tree</li>
<li>There is a unique simple path between every pair of vertices.</li>
<li>Adding an edge between nonadjacent nodes in a tree creates a graph with a cycle</li>
<li>Removing any edge disconnect the graph</li>
<li>If the tree has at least two vertices, then it has at least two leaves.</li>
<li>The number of vertices in a tree is one larger than the number of edges.</li>
</ol>
<h2 id="spanning-trees">Spanning trees</h2>
<dl>
<dt>Spanning tree</dt>
<dd>A spanning tree is a subgraph of a connected graph that has the same vertices as the graph.</dd>
</dl>
<p>Every connected graph contains a spanning tree.</p>
<h2 id="minimum-weight-spanning-trees">Minimum Weight Spanning Trees</h2>
<p>Spanning trees are important because they connect every node of a graph with the smallest possible number of edges.<br>
However in the real world there are often costs associated with the edges of the graph.<br>
The <em><strong>weight</strong></em> of a spanning tree is the sum of weights of the edges in the tree.</p>
<dl>
<dt>Min-weight Spanning Tree</dt>
<dd>The <em><strong>min-weight spanning tree</strong></em> (MST) of an edge-weighted graph G is the spanning tree of G with the smallest possible sum of edge weights.</dd>
</dl>
<h3 id="algorithm-to-find-mst">Algorithm to Find MST</h3>
<dl>
<dt>Algorithm 1</dt>
<dd>Grow a tree one edge at a time by adding the minimum weight edge possible to the tree, making sure that you have a tree at each step.</dd>
<dt>Algorithm 2</dt>
<dd>Grow a subgraph one edge at a time by adding the minimum-weight edge possible to the subgraph, making sure that you have an acyclic subgraph at each step.</dd>
</dl>
<h1 id="planner-graphs">Planner Graphs</h1>
<p>A <em><strong>drawing of a graph in the plane</strong></em> consists of an assignment of vertices to distinct points in the plane and an assignment of edges to smooth, non-self-intersecting curves in the plane</p>
<p>The drawing is <em><strong>planer</strong></em>, a <em><strong>planner drawing</strong></em>, if none of the curves “cross”; That is, if the only points that appear on more than one curves are the vertex points.</p>
<p>A <em><strong>planner graph</strong></em> is a graph that has a planer drawing.</p>
<h2 id="faces">Faces</h2>
<p>In a planar drawing of a graph, the curves corresponding to the edges divide up the plane into <em><strong>connected regions</strong></em>. These regions are called the <em><strong>continuous faces</strong></em> of the drawing. The vertices along the boundary of each of the faces form a cycle.</p>
<p>The face on the outside that stretch on to infinity is called the <em><strong>outside face</strong></em>.</p>
<p><em><strong>bridge</strong></em><br>
<em><strong>dongle</strong></em></p>
<p><em><strong>Planar embedding</strong></em></p>
<h2 id="euler-formula">Euler formula</h2>
<blockquote>
<p>If a connected graph has a planar embedding, then<br>
<span class="katex--display"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><mi>v</mi><mo>−</mo><mi>e</mi><mo>+</mo><mi>g</mi><mo>=</mo><mn>2</mn></mrow><annotation encoding="application/x-tex">v - e + g = 2</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.66666em; vertical-align: -0.08333em;"></span><span class="mord mathnormal" style="margin-right: 0.03588em;">v</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.66666em; vertical-align: -0.08333em;"></span><span class="mord mathnormal">e</span><span class="mspace" style="margin-right: 0.222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right: 0.222222em;"></span></span><span class="base"><span class="strut" style="height: 0.625em; vertical-align: -0.19444em;"></span><span class="mord mathnormal" style="margin-right: 0.03588em;">g</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.64444em; vertical-align: 0em;"></span><span class="mord">2</span></span></span></span></span></span></p>
</blockquote>
<pre><code>slkfjslkfj
	klsfksjflsfjslkf	
</code></pre>

