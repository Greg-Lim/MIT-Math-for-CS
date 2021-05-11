<dl>
<dt>Proposition</dt>
<dd>A proposition is a statement that is either true or false</dd>
</dl>
<p>Variables such a P and Q are often used in place of a proposition.</p>
<h1 id="compound-propositions">Compound Propositions</h1>
<h2 id="implies">Implies</h2>

<table>
<thead>
<tr>
<th>P</th>
<th>Q</th>
<th>P IMPLIES Q</th>
</tr>
</thead>
<tbody>
<tr>
<td>T</td>
<td>T</td>
<td>T</td>
</tr>
<tr>
<td>T</td>
<td>F</td>
<td>F</td>
</tr>
<tr>
<td>F</td>
<td>T</td>
<td>T</td>
</tr>
<tr>
<td>F</td>
<td>F</td>
<td>T</td>
</tr>
</tbody>
</table><h2 id="iff---if-and-only-if">IFF - If and only if</h2>
<p>The proposition “P if and only if Q” asserts P and Q are logically equivalent.<br>
Both True or Both False.</p>
<h2 id="notations">Notations</h2>

<table>
<thead>
<tr>
<th>English</th>
<th>Symbol Notation</th>
<th>Symbol</th>
</tr>
</thead>
<tbody>
<tr>
<td>NOT§</td>
<td>¬P</td>
<td>¬</td>
</tr>
<tr>
<td>P AND Q</td>
<td>P ∧ Q</td>
<td>∧</td>
</tr>
<tr>
<td>P OR Q</td>
<td>P ∨ Q</td>
<td>∨</td>
</tr>
<tr>
<td>P IMPLIES Q</td>
<td>P → Q</td>
<td>→</td>
</tr>
<tr>
<td>IF P THEN Q</td>
<td>P → Q</td>
<td>→</td>
</tr>
<tr>
<td>P IFF Q</td>
<td>P ↔ Q</td>
<td>↔</td>
</tr>
</tbody>
</table>
<table>
<thead>
<tr>
<th>English</th>
<th>Symbol Notation</th>
</tr>
</thead>
<tbody>
<tr>
<td>For All</td>
<td>∀</td>
</tr>
<tr>
<td>There Exist</td>
<td>∃</td>
</tr>
<tr>
<td>Non-negative Integer</td>
<td>ℕ OR N</td>
</tr>
<tr>
<td>Positive Integer</td>
<td>Z+</td>
</tr>
<tr>
<td>Element of</td>
<td>∈</td>
</tr>
<tr>
<td>Equal by Definition</td>
<td>::=</td>
</tr>
<tr>
<td>IF P THEN Q</td>
<td>P → Q</td>
</tr>
<tr>
<td>P IFF Q</td>
<td>P ↔ Q</td>
</tr>
</tbody>
</table><h1 id="predicates">Predicates</h1>
<dl>
<dt>Predicate</dt>
<dd>A predicate is a proposition whose truth depends on the value of one or more variables.</dd>
</dl>
<p>Often named with a letter<br>
e.g. P(n) ::= “n is a perfect square”</p>
<ul>
<li>A predicate is not a function and is either true or false depending on the input</li>
<li>An assertion that a predicate is always true is called a <em>universally quantified</em> statement</li>
<li>An assertion that a predicate is sometimes true is called a <em>existentially quantified</em> statement</li>
</ul>
<h1 id="some-identities">Some Identities</h1>
<p>∀x ∈ D ∃y ∈ D. Q(x, y)<br>
Can be written as<br>
∀x∃y. Q(x, y)</p>
<p>NOT(∀x. P(x)) is equivalent to ∃x. NOT(P(x))</p>
<p>NOT(∃x. P(x)) IFF ∀x. NOT(P(x))</p>
<h1 id="validity">Validity</h1>
<dl>
<dt>Validity</dt>
<dd>A propositional formula is called valid when it evaluates to T no matter what truth values are assigned to the individual propositional variables</dd>
</dl>
<h1 id="satisfiability">Satisfiability</h1>
<dl>
<dt>Satisfiability</dt>
<dd>A proposition is satisfiable if some setting of the variables makes the proposition true.<br>
P AND NOT Q is satisfiable<br>
P AND NOT P is not satisfiable<br>
A problem of deciding whether a proposition is satisfiable called a SAT.</dd>
</dl>

