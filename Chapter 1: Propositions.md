Proposition
: A proposition is a statement that is either true or false

Variables such a P and Q are often used in place of a proposition.

# Compound Propositions

## Implies

| P   | Q   | P IMPLIES Q |
| --- | --- | --- |
| T   | T   | T   |
| T   | F   | F   |
| F   | T   | T   |
| F   | F   | T   |

## IFF - If and only if

The proposition "P if and only if Q" asserts P and Q are logically equivalent.
Both True or Both False.

## Notations

| English | Symbol Notation | Symbol |
| --- | --- | --- |
| NOT(P) | ¬P  | ¬   |
| P AND Q | P ∧ Q | ∧   |
| P OR Q | P ∨ Q | ∨   |
| P IMPLIES Q | P → Q | →   |
| IF P THEN Q | P → Q | →   |
| P IFF Q | P ↔ Q | ↔   |

| English | Symbol Notation |
| --- | --- |
| For All | ∀   |
| There Exist | ∃   |
| Non-negative Integer | ℕ OR N |
| Positive Integer | Z+  |
| Element of | ∈   |
| Equal by Definition | ::= |
| IF P THEN Q | P → Q |
| P IFF Q | P ↔ Q |

# Predicates

Predicate
: A predicate is a proposition whose truth depends on the value of one or more variables.

Often named with a letter
e.g. P(n) ::= "n is a perfect square"

- A predicate is not a function and is either true or false depending on the input
- An assertion that a predicate is always true is called a *universally quantified* statement
- An assertion that a predicate is sometimes true is called a *existentially quantified* statement

# Some Identities

∀x ∈ D ∃y ∈ D. Q(x, y)
Can be written as
∀x∃y. Q(x, y)

NOT(∀x. P(x)) is equivalent to ∃x. NOT(P(x))

NOT(∃x. P(x)) IFF ∀x. NOT(P(x))

# Validity
Validity
: A propositional formula is called valid when it evaluates to T no matter what truth values are assigned to the individual propositional variables

# Satisfiability

Satisfiability
: A proposition is satisfiable if some setting of the variables makes the proposition true.
    P AND NOT Q is satisfiable
    P AND NOT P is not satisfiable
    A problem of deciding whether a proposition is satisfiable called a SAT.
