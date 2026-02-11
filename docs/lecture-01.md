# Lecture 1

## Probability

**Definition**: a likelihood from 0 (never) to 1 (always). Usually denoted as the function $\mathbb{P}$.

## Sample Space

**Definition**: a set of all possible outcomes. For example for a coin: $\{ Head, Tail \}$.

## Events

**Definition**: a subset of the [sample space](#sample-space). For example with a D6, we have the [sample space](#sample-space) $S$: $\{ 1, 2, ..., 6 \}$. Then an event $E$ can be "dice is odd", which would mean: $E = \{ 1, 3, 5 \}$.

## Disjoint

**Definition**: two sets $A$ and $B$ are disjoint if $A\cap B = \emptyset$.

## Exhaustive

**Definition**: two sets $A$ and $B$ are exhaustive if $A\cup B = S$ where $S$ is the [sample space](#sample-space).

## Adding Probabilities of [Events](#events)

**Definition**: let $A, B \subseteq S$ be any [event](#event), then $\mathbb{P}(A\cup B) = \mathbb{P}(A) + \mathbb{P}(B) - \mathbb{P}(A \cap B)$. If $A$ and $B$ are **[disjoined](#disjoint)** [events](#events), then $\mathbb{P}(A\cup B) = \mathbb{P}(A) + \mathbb{P}(B)$.

## Compliment Rule

**Definition**: Let $A \subseteq S$ be an [event](#event), since $A \cup A^c = S$ we have that $\mathbb{P}(A^c) = 1 - \mathbb{P}(A)$.

## Independent

**Definition**: Let $A, B \subseteq S$ be a [events](#event). If $\mathbb{P}(A\cap B) = \mathbb{P}(A)\cdot\mathbb{P}(B)$ holds, then the [events](#event) $A$ and $B$ are independent

## Equally likely outcomes

**Definition**: Assume that the [sample space](#sample-space) has a finite amount ($n$) of equally likely value: $S = \{ s_1, s_2, ..., s_n \}$. Then we say that all events are equally likely if $\mathbb{P}(s_1) = \mathbb{P}(s_2) = ... = \mathbb{P}(s_n) = {1\over n}$.

## Sampling without replacement

**Definition**: Sampling without replacement means that after each draw, the sampled item is removed from the population. Aka The same object can only appear once in the drawn sample.

## Sampling with replacement

**Definition**: Sampling without replacement means that after each draw, the sampled item is put back into the population. Aka The same object can only appear more then once in the drawn sample.
