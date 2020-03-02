# What is a Knowledge Representation?

> **Authors:** Randall Davis, Howard Shrobe, Peter Szolovitz
>
> **Published:** 1993
>
> **Source:** https://aaai.org/ojs/index.php/aimagazine/article/view/1029



## Introduction

### Roles of a knowledge representation (KR)

The notion of a KR may be best described by its five roles:

1. It is most fundamentally a *surrogate*, i.e. a substitute for the thing it represents. It is used by an entity to determine consequences via thinking rather than acting.
2. It is a set of *ontological commitments*, i.e. the terms and clauses that I think about the world with.
3. It is a *fragmentary theory of reasoning*, expressed in terms of three components:
   1. the representation's fundamental conception of intelligent reasoning (i.e. its calculus);
   2. the set of inferences that the representation sanctions; and 
   3. the set of inferences that it recommends
4. It is a *medium for pragmatically efficient computation*, i.e. the computational environment on which thinking is accomplished.
   - The representation contributes to this by organising information to facilitate making recommended inferences
5. It is a medium of human expression; a language.



### Consequences of the roles and their diversity

1. Each role requires something slightly different from a representation, which leads to different sets of properties that we may want a representation to have.
2. The roles are believed to provide a framework for characterising a wide variety of representations, depending on how each representation views each role.
3. Previous disagreements about representation are usefully disentangled when all five roles are given appropriate consideration.
4. For research, this view of representations provides a broad perspective on what's important about a representation. For practice, it is a reminder about the inspirations and sources of power for a variety of representations.



# Terminology and Perspective

- **Inference**: any way to get new expressions from old
- **KR technologies**: basic tools such as *logic, rules, frames, and semantic nets*.
- KRs are commonly built on *multiple levels of languages*, typically with one of the knowledge representation technologies at the bottom level.
  - e.g. Hayes's ontology of liquids (1978). It is at one level a representation composed of concepts like pieces of space -- portals, faces, sides, and so on. The next, more primitive, and bottom level of language is first-order logic, e.g. $In(s_1,s_2)$ expresses that space $s_1$ is contained in $s_2$.
- This view is useful in part because it allows this discussion to concentrate largely on KR technologies. As they are a fundamental component of all KRs, hey are widely familiar to the community and encounter all the issues central to KRs of any variety.



## Roles of KR

### Role 1: A Surrogate

### Role 2: A Set of Ontological Commitments

### Role 3: A Fragmentary Theory of Reasoning

### Role 4: A Medium for Efficient Computation

### Role 5: A Medium of Human Expression



## Consequences

