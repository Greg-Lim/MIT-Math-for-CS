<p>This chapter is on how to proof theorems.</p>
<h1 id="the-axiomatic-method">The Axiomatic Method</h1>
<ul>
<li>A <em><strong>theorems</strong></em> is an Important proposition</li>
<li>A <em><strong>lemma</strong></em> is a preliminary proposition useful for proving later propositions</li>
<li>A <em><strong>corollary</strong></em> is a proposition  that follows in just a few logical steps from a lemma or a theorem</li>
</ul>
<p><em><strong>Modus ponens</strong></em> is a fundamental inference rule that says a proof of P together with a proof that P IMPLIES Q is a proof of Q.</p>
<p><span class="katex--display"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><mfrac><mtext>P;&nbsp;P&nbsp;IMPLIES&nbsp;Q</mtext><mtext>Q</mtext></mfrac></mrow><annotation encoding="application/x-tex">
\frac{\text{P; P IMPLIES Q}}
{\text{Q}}
</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 2.24077em; vertical-align: -0.88044em;"></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 1.36033em;"><span class="" style="top: -2.314em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord text"><span class="mord">Q</span></span></span></span><span class="" style="top: -3.23em;"><span class="pstrut" style="height: 3em;"></span><span class="frac-line" style="border-bottom-width: 0.04em;"></span></span><span class="" style="top: -3.677em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord text"><span class="mord">P;&nbsp;P&nbsp;IMPLIES&nbsp;Q</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.88044em;"><span class=""></span></span></span></span></span><span class="mclose nulldelimiter"></span></span></span></span></span></span></span></p>
<p>When the statements above the line, called the <em><strong>antecedents</strong></em> (an-ti-see-dents), are proved, the statement below the line, <em><strong>conclusion</strong></em> or <em><strong>consequent</strong></em>, can be considered proved.</p>
<h1 id="prove-by-case">Prove by Case</h1>
<p>Breaking a complicated proof into cases and proving that each case separately.</p>
<h2 id="method-1-proof-all-cases">Method 1: Proof all cases</h2>
<p><em>Proof.</em> Proof is by case analysis.</p>
<ol>
<li>Show that your cases covered all cases.</li>
<li>Show that the theorem holds for all cases.</li>
</ol>
<h1 id="prove-by-implication">Prove by Implication</h1>
<p>Propositions in the form “If P, then Q” are called implications. Some written as “P implies Q” or “P → Q”.</p>
<p>If P, then Q.</p>
<h2 id="method-1-assume-p-is-true">Method 1: Assume P is true</h2>
<p><em>Proof.</em> Proof by assume P is true</p>
<ol>
<li>Assume P (is true)</li>
<li>Proof Q is true for P</li>
</ol>
<h2 id="method-2-prove-the-contra-positive">Method 2: Prove the Contra-positive</h2>
<p>Instead of P implies Q, we prove Not Q implies NOT P<br>
<em>Proof.</em> Proof the Contra-positive</p>
<ol>
<li>Write, “We prove the contra-positive”, and state the contra-positive</li>
<li>Proceed with Method 1</li>
</ol>
<h1 id="proving-an-if-and-only-if">Proving an “If and only if”</h1>
<p>P IFF Q</p>
<h2 id="method-1-prove-each-statement-implies-the-other">Method 1: Prove each statement implies the other</h2>
<p>P IFF Q is equivalent to P implies Q and Q implies P.</p>
<ol>
<li>Write, “We prove P implies Q and vice-versa.”</li>
<li>Prove P implies Q</li>
<li>Prove Q implies P</li>
</ol>
<h2 id="method-2-construct-chain-of-iffs">Method 2: Construct chain of IFFs</h2>
<ol>
<li>Write, “We construct a chain of if-and-only-if implications”</li>
<li>Prove P is equivalent to statement 1 and statement 2 and so on to Q.</li>
</ol>
<h1 id="proof-by-contradiction">Proof by contradiction</h1>
<p>Aka indirect proof<br>
Show that if a proposition were false, then some false fact would be true. Since false facts cannot be true, the proposition is true.</p>
<h2 id="method-1">Method 1</h2>
<ol>
<li>Write, “We use proof by contradiction.”</li>
<li>Write, “Suppose P is false”</li>
<li>Deduce something known to be false.</li>
<li>Write, “This is a contradiction. There fore, P must be true”</li>
</ol>
<h1 id="proofs-about-sets">Proofs about Sets</h1>
<h2 id="sets-definition">Sets Definition:</h2>
<ul>
<li>A <em><strong>set</strong></em> is a bunch of objects called <em><strong>elements</strong></em>.</li>
<li>All elements is either in a set or not in a set.</li>
<li>A set only contain each element once. {x} ={x,x}</li>
</ul>

<table>
<thead>
<tr>
<th>symbol</th>
<th>set</th>
<th>elements</th>
</tr>
</thead>
<tbody>
<tr>
<td>∅</td>
<td>the empty set</td>
<td>none</td>
</tr>
<tr>
<td>N or ℕ</td>
<td>non-negative integers</td>
<td>{0, 1, 2, …}</td>
</tr>
<tr>
<td>Z or ℤ</td>
<td>integers</td>
<td>{…, -2, -1, 0, 1, 2, …}</td>
</tr>
<tr>
<td>Q or ℚ</td>
<td>rational numbers</td>
<td>1/2, 16, …</td>
</tr>
<tr>
<td>R or ℝ</td>
<td>real numbers</td>
<td>π, e, 9, sqrt(2), …</td>
</tr>
<tr>
<td>C or ℂ</td>
<td>complex numbers</td>
<td>i, …</td>
</tr>
</tbody>
</table><ul>
<li>A superscript “+” restrict a set to positive elements. And “-” for negative elements</li>
</ul>
<h2 id="set-notations">Set Notations</h2>
<ul>
<li>S ⊆ T : S is a subset of T.</li>
<li>S ⊂ T : S is a proper subset of T.</li>
<li>A ⊆ A but A ⊄ A</li>
<li>X ∪ Y : X union Y, consist of all elements that appear in X or Y.</li>
<li>X ∩ Y : X intersect Y, consist of all elements that appear in both X and Y.</li>
</ul>
<h2 id="compliment-set">Compliment set</h2>
<p>For a domain, D; For a subset A of D; We define ¬A to be all elements of D not in A. ¬A ::= D - A. Set ¬A is called the <em><strong>complement</strong></em> of A.</p>
<p>For 2 sets, A and B, they are said to be <em><strong>disjoint</strong></em> iff they have no elements in common. A ∩ B = ∅. A ⊆ ¬B</p>
<h2 id="carnality">Carnality</h2>
<p>The <em><strong>carnality</strong></em> of a set A is the number of elements in set A and is denoted by |A|.</p>
<h2 id="the-power-set">The Power Set</h2>
<p>The set of all subsets of set A, is called the <em><strong>power set</strong></em>, P(A) of A.</p>
<ul>
<li>B ∈ of P(A) iff B ⊆ A.</li>
<li>P({1,2}) = {∅, {1}, {2}, {1,2}}</li>
<li>A is finite, |P(A)| = 2^|A|</li>
</ul>
<h2 id="sequences">Sequences</h2>
<ul>
<li>A <em><strong>sequences</strong></em> is a list of objects called <em><strong>terms</strong></em> or <em><strong>components</strong></em>.</li>
<li>Sequence can have repeating terms.</li>
<li>The order of a sequence matters</li>
<li>An empty sequence is denoted by λ. (∅ for empty sets)</li>
</ul>
<h2 id="cross-product">Cross Product</h2>
<p>A product of Sets, S1 x S2 x S3 … , is a new set of sequences.<br>
A x B  = {(a, b) :  a ∈ A  and  b ∈ B}<br>
e.g. {a,b} * {c,d} = {(a, c), (a, d), (b, c) (b, d)}</p>
<h2 id="set-builder-notation">Set Builder Notation</h2>
<ul>
<li>Sets can be stated explicitly or by taking union and intersections, etc., of easily-described sets.</li>
<li>The idea is to define a set using a predicate.</li>
<li>A set that consist of all values that make the predicate true.<br>
e.g. A ::= {n ∈ of N | n is prime and n = 4k + 1 for some integer k}</li>
</ul>
<h2 id="proving-set-equalities">Proving Set Equalities</h2>
<ul>
<li>Two sets are defined to be equal iff they both contains the same elements, z.</li>
</ul>
<h3 id="identities">Identities</h3>
<ul>
<li>A ∩ (B ∪ C) = (A ∩ B) ∪ (A ∩ C);</li>
</ul>
<h1 id="good-proofs-in-practice">Good Proofs in Practice</h1>
<h2 id="how-to-write-a-good-proof">How to write a good Proof:</h2>
<ul>
<li>State your game plan</li>
<li>Keep linear flow</li>
<li>A proof is like an essay, not a calculation</li>
<li>Avoid excessive symbolism</li>
<li>Revice and simplify</li>
<li>Introduce notation thoughtfully</li>
<li>Structure long proofs</li>
<li>Be wary of “Obvious”</li>
<li>Finish the proof</li>
</ul>

