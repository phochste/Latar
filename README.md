# Latar

A mini [RDF Surfaces](https://w3c-cg.github.io/rdfsurfaces/) playground in Prolog.

Latar, Indonesian for 'surface', is an attempt to create a new RDF Surfaces implementation in Prolog using Peirce's [Existential Graph](https://en.wikipedia.org/wiki/Existential_graph) methods.

# Install

Install SWIPL : https://www.swi-prolog.org/download/stable

# Run

`./test.sh`

# Examples

## Alpha

Propositional logic

- alice : a simple conditional `(Alice a Human) -> (Alice a Person)` 
- disjunction : a simple disjunction `(Alice likes Coffee) OR (Alice likes Tea)`
- nested_negation : 4 level deep negation eventually is an assertion
- lists : a simple lists test
- built-in : a simple built-in test

## Beta

First-order logic

- socrates : an OWL subClassOf example
- socrates2 : socrates but with two subClassOf statements
- abc : disjunction example
- abcd : disjunction plus triple nested negative surface example

## Notation3 (N3)

The N3 serialization of RDF Surfaces can be used using the `latar` command. We use 
[EYE](https://github.com/eyereasoner/eye) as precompiler from N3 to Prolog, run the Latar code, and translate back from Prolog to N3.

```
$ latar n3/socrates.n3s
<urn:example:test> <urn:example:is> true.
```
