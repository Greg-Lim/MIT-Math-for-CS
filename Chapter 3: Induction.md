This chapter is on using induction to proof.
# Well-Ordering Principle
- Every non-empty set of non-negative integer have a smallest element.

## Proof - Well order proof
1.  Define the set, C, of counter examples to P being true.
    C ::= {n ∈ N| P(n) is false}
2.  Use proof by contradiction and assume C is non-empty.
3.  By using well ordering principle, where will be a smallest element, n, in C.
4.  Reach a contradiction, usually by proving that there is a smaller value in C
5.  Conclude that C must be empty and no counter example exist.

# Ordinary induction

## Principle of induction
Let P(n) be the predicate. If
- P(0) is true, and
- P(n) implies P(n+1), for all non-negative integer, n

P(m) is true for all non-negative integer m

### Induction rule:
$$
\frac{\text{P(0), ∀n ∈ N. P(n) IMPLIES P(n+1)}}
{\text{∀m ∈ N. P(m)}}
$$
## Proof - Ordinary Induction

1.  State that the proof uses induction
2.  Define the appropriate predicate P(n)
    - Usually the proposition
    - Sometimes the induction hypothesis have multiple variable. Indicated which is n.
3.  Prove P(0) is true. The base case.
4.  Prove P(n) implies P(n+1) for all non-negative intergers. The inductive step.
    - Assume P(n) is true
    - Use the assumption to prove P(n+1) is true
5.  Invoke induction

If the current inductive hypothesis cannot prove the statement, we can use a stronger inductive hypothesis to prove it.
- With a stronger hypothesis, We can assume a stronger statement is true

# Invariant
Invariant is a property that does not change through a series of steps.

## Proof - Invariant Method

To prove that some property, "NICE" holds for every step of the process.

1.  Define P(t) to be a predicate that "NICE" holds immediately after step t
2.  Show that P(0) is true, "NICE" holds from the start.
3.  Show that ∀t ∈ N. P(t) IMPLIES P(t+1).

# Strong Induction
Strong induction us useful when the predicate, P(n+1) naturally depends on P(a) where a < n.

## Principle of Strong Induction
Let P(n) be the predicate.
If
- P(0) is true
- for all n ∈ N, P(0), P(1), P(2), ..., P(n) together imply P(n+1)
    then P(n) is true for all n ∈ N

## Strong Induction Rule

$$
\frac{\text{P(0), ∀n ∈ N. (P(0) AND P(1) AND ... AND P(m)) IMPLIES P(N+1)}}
{\text{∀m ∈ N. P(m)}}
$$

## Proof - Strong Induction
Is similar to Ordinary Induction except:
- You should state your proof as strong induction
- You can assume P(0), P(1), ..., P(n) are all true instead of just P(n)

# Structural Induction

## Recursive Data Types

Recursive have two types.

- Base case - does not depend on anything
- Constructor type - depends on previous case

## Structural Induction on Recursive Data Types
Structural induction is a method for proving some property, P, holds for all element is a recursivly defined data type.

## Proof
- Prove for the base case of the definition
- Prove P for all constructor cases of the definition, assuming that it is true for the component data items).
