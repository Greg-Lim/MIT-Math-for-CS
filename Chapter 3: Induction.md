<p>This chapter is on using induction to proof.</p>
<h1 id="well-ordering-principle">Well-Ordering Principle</h1>
<ul>
<li>Every non-empty set of non-negative integer have a smallest element.</li>
</ul>
<h2 id="proof---well-order-proof">Proof - Well order proof</h2>
<ol>
<li>Define the set, C, of counter examples to P being true.<br>
C ::= {n ∈ N| P(n) is false}</li>
<li>Use proof by contradiction and assume C is non-empty.</li>
<li>By using well ordering principle, where will be a smallest element, n, in C.</li>
<li>Reach a contradiction, usually by proving that there is a smaller value in C</li>
<li>Conclude that C must be empty and no counter example exist.</li>
</ol>
<h1 id="ordinary-induction">Ordinary induction</h1>
<h2 id="principle-of-induction">Principle of induction</h2>
<p>Let P(n) be the predicate. If</p>
<ul>
<li>P(0) is true, and</li>
<li>P(n) implies P(n+1), for all non-negative integer, n</li>
</ul>
<p>P(m) is true for all non-negative integer m</p>
<h3 id="induction-rule">Induction rule:</h3>
<p><span class="katex--display"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><mfrac><mtext>P(0),&nbsp;∀n&nbsp;∈&nbsp;N.&nbsp;P(n)&nbsp;IMPLIES&nbsp;P(n+1)</mtext><mtext>∀m&nbsp;∈&nbsp;N.&nbsp;P(m)</mtext></mfrac></mrow><annotation encoding="application/x-tex">
\frac{\text{P(0), ∀n ∈ N. P(n) IMPLIES P(n+1)}}
{\text{∀m ∈ N. P(m)}}
</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 2.363em; vertical-align: -0.936em;"></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 1.427em;"><span class="" style="top: -2.314em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord text"><span class="mord">∀m&nbsp;∈&nbsp;N.&nbsp;P(m)</span></span></span></span><span class="" style="top: -3.23em;"><span class="pstrut" style="height: 3em;"></span><span class="frac-line" style="border-bottom-width: 0.04em;"></span></span><span class="" style="top: -3.677em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord text"><span class="mord">P(0),&nbsp;∀n&nbsp;∈&nbsp;N.&nbsp;P(n)&nbsp;IMPLIES&nbsp;P(n+1)</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.936em;"><span class=""></span></span></span></span></span><span class="mclose nulldelimiter"></span></span></span></span></span></span></span></p>
<h2 id="proof---ordinary-induction">Proof - Ordinary Induction</h2>
<ol>
<li>State that the proof uses induction</li>
<li>Define the appropriate predicate P(n)
<ul>
<li>Usually the proposition</li>
<li>Sometimes the induction hypothesis have multiple variable. Indicated which is n.</li>
</ul>
</li>
<li>Prove P(0) is true. The base case.</li>
<li>Prove P(n) implies P(n+1) for all non-negative intergers. The inductive step.
<ul>
<li>Assume P(n) is true</li>
<li>Use the assumption to prove P(n+1) is true</li>
</ul>
</li>
<li>Invoke induction</li>
</ol>
<p>If the current inductive hypothesis cannot prove the statement, we can use a stronger inductive hypothesis to prove it.</p>
<ul>
<li>With a stronger hypothesis, We can assume a stronger statement is true</li>
</ul>
<h1 id="invariant">Invariant</h1>
<p>Invariant is a property that does not change through a series of steps.</p>
<h2 id="proof---invariant-method">Proof - Invariant Method</h2>
<p>To prove that some property, “NICE” holds for every step of the process.</p>
<ol>
<li>Define P(t) to be a predicate that “NICE” holds immediately after step t</li>
<li>Show that P(0) is true, “NICE” holds from the start.</li>
<li>Show that ∀t ∈ N. P(t) IMPLIES P(t+1).</li>
</ol>
<h1 id="strong-induction">Strong Induction</h1>
<p>Strong induction us useful when the predicate, P(n+1) naturally depends on P(a) where a &lt; n.</p>
<h2 id="principle-of-strong-induction">Principle of Strong Induction</h2>
<p>Let P(n) be the predicate.<br>
If</p>
<ul>
<li>P(0) is true</li>
<li>for all n ∈ N, P(0), P(1), P(2), …, P(n) together imply P(n+1)<br>
then P(n) is true for all n ∈ N</li>
</ul>
<h2 id="strong-induction-rule">Strong Induction Rule</h2>
<p><span class="katex--display"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><mfrac><mtext>P(0),&nbsp;∀n&nbsp;∈&nbsp;N.&nbsp;(P(0)&nbsp;AND&nbsp;P(1)&nbsp;AND&nbsp;...&nbsp;AND&nbsp;P(m))&nbsp;IMPLIES&nbsp;P(N+1)</mtext><mtext>∀m&nbsp;∈&nbsp;N.&nbsp;P(m)</mtext></mfrac></mrow><annotation encoding="application/x-tex">
\frac{\text{P(0), ∀n ∈ N. (P(0) AND P(1) AND ... AND P(m)) IMPLIES P(N+1)}}
{\text{∀m ∈ N. P(m)}}
</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 2.363em; vertical-align: -0.936em;"></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height: 1.427em;"><span class="" style="top: -2.314em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord text"><span class="mord">∀m&nbsp;∈&nbsp;N.&nbsp;P(m)</span></span></span></span><span class="" style="top: -3.23em;"><span class="pstrut" style="height: 3em;"></span><span class="frac-line" style="border-bottom-width: 0.04em;"></span></span><span class="" style="top: -3.677em;"><span class="pstrut" style="height: 3em;"></span><span class="mord"><span class="mord text"><span class="mord">P(0),&nbsp;∀n&nbsp;∈&nbsp;N.&nbsp;(P(0)&nbsp;AND&nbsp;P(1)&nbsp;AND&nbsp;...&nbsp;AND&nbsp;P(m))&nbsp;IMPLIES&nbsp;P(N+1)</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height: 0.936em;"><span class=""></span></span></span></span></span><span class="mclose nulldelimiter"></span></span></span></span></span></span></span></p>
<h2 id="proof---strong-induction">Proof - Strong Induction</h2>
<p>Is similar to Ordinary Induction except:</p>
<ul>
<li>You should state your proof as strong induction</li>
<li>You can assume P(0), P(1), …, P(n) are all true instead of just P(n)</li>
</ul>
<h1 id="structural-induction">Structural Induction</h1>
<h2 id="recursive-data-types">Recursive Data Types</h2>
<p>Recursive have two types.</p>
<ul>
<li>Base case - does not depend on anything</li>
<li>Constructor type - depends on previous case</li>
</ul>
<h2 id="structural-induction-on-recursive-data-types">Structural Induction on Recursive Data Types</h2>
<p>Structural induction is a method for proving some property, P, holds for all element is a recursivly defined data type.</p>
<h2 id="proof">Proof</h2>
<ul>
<li>Prove for the base case of the definition</li>
<li>Prove P for all constructor cases of the definition, assuming that it is true for the component data items).</li>
</ul>

