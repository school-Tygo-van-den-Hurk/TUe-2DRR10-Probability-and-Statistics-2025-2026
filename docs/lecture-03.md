# Lecture 3

This lecture is about discreet distributions, see [lecture 5](./lecture-05.md) for continuous distributions.

## Bernoulli random variable

### Interpretation

A Bernoulli random variable $\text{Ber}(p)$ models experiments with two possible outcomes.

### Definition

a Bernoulli random variable $X$ is a random variable with range $\{ 0, 1 \}$. For any parameter $p \in (0,1)$, the p.m.f. of a Bernoulli random variable with parameter $p$ is given by:

$$\mathbb{P}(X = 1) = p\wedge\mathbb{P}(X = 0) = 1 - p$$

We write $X \sim \text{Ber}(p)$ for this distribution.

### Attributes

| **Attribute** | **Value**                                          |
| ------------- | -------------------------------------------------- |
| Range         | $\{ 0, 1 \}$                                       |
| Parameters    | $p \in (0, 1)$                                     |
| Notation      | $X \sim \text{Ber}(p)$                             |
| P.m.f.        | $\mathbb{P}(X = 0) = 1 − p, \mathbb{P}(X = 1) = p$ |
| Mean          | $\mathbb{E}[X] = p$                                |
| Variance      | $Var(X) = p \cdot (1 − p)$                         |

## Binomial random variable

### Interpretation

The binomial distribution $\text{Bin}(n,p)$ models the number of successes in n independent Bernoulli experiments each of which has success probability $p$. Parameters:

- $n$: the number of Bernoulli experiments (upper bound on the number of successes).
- $p$: success probability in each single Bernoulli experiment.

### Definition

A Binomial random variable $X$ with parameters $n\in\mathbb{N}$ and $p\in(0,1)$ has range $\{ 0, 1, ..., n \}$. It is defined by a p.m.f. of the form:

$$\mathbb{P}(X = k) = \binom{n}{k} \cdot p^k \cdot (1 −p)^{n−k}$$

We write $X \sim \text{Bin}(n, p)$.

### Attributes

| **Attribute** | **Value**                                              |
| ------------- | ------------------------------------------------------ |
| Range         | $\{ 0, 1, ..., n \}$                                   |
| Parameters    | $n \in \mathbb{N} \wedge p \in (0, 1)$                 |
| Notation      | $X \sim \text{Bin}(n, p)$                              |
| P.m.f.        | $P(X = k) = \binom{n}{k} \cdot p^k \cdot (1 −p)^{n−k}$ |
| Mean          | $\mathbb{E}[X] = n \cdot p$                            |
| Variance      | $Var(X) = n \cdot p \cdot (1 − p)$                     |

## Discrete Uniform distribution

### Definition

Let $X$ be a random variable $X$ with a finite range $\{ x_1, ..., x_n \}$. $X$ is said to have a discrete uniform distribution if the p.m.f. of $X$ has the form:

$$\mathbb{P}(X = x_i) = {1\over n}$$

We write $X \sim \text{Unif}(\{ x_1, ..., x_n \})$.

### Attributes

| **Attribute** | **Value**                                   |
| ------------- | ------------------------------------------- |
| Range         | $\{ a, ..., b \}$                           |
| Parameters    | $a, b \in\mathbb{n}                         |
| Notation      | $X \sim \text{Unif}(\{ x_1, ..., x_n \})$   |
| P.m.f.        | $\mathbb{P}(X = k) = { 1 \over b - a + 1 }$ |
| Mean          | $\mathbb{E}[X] = { a + b \over 2 }$         |
| Variance      | $Var(X) = { (b- a + 1)^2 - 1 \over 12 }$    |

## Geometric distribution

### Interpretation

The geometric distribution Geom(p) models the number of trials in a sequence of independent Bernoulli experiments with success probability $p$ until (and including) you see the first success.

Parameters:

- $p$: success probability in each single Bernoulli experiment

### Definition

A Geometric random variable $X$ with parameter $p\in(0, 1)$ has range $\mathbb{N}$. It is defined by a p.m.f. of the form: 

$$\mathbb{P}(X = k) = p(1 − p)^{k−1} \text{ for }k = 1, 2, 3, ...$$

We write $X \sim \text{Geom}(p)$.

### Attributes

| **Attribute** | **Value**                             |
| ------------- | ------------------------------------- |
| Range         | $\mathbb{N}$                          |
| Parameters    | $p\in(0,1)$                           |
| Notation      | $X \sim \text{Geom}(p)$               |
| P.m.f.        | $\mathbb{P}(X = k) = p (1 - p)^{k-1}$ |
| Mean          | $\mathbb{E}[X] = { 1 \over p }$       |
| Variance      | $Var(X) = { 1 - p \over p^2 }$        |

## Negative binomial distribution

### Interpretation

The negative Binomial distribution $\text{NegBin}(r, p)$ models the number of independent Bernoulli trials with success probability $p$ until you see the $r^{th}$ success.

Parameters:

- $r$: number of successes you want to observe.
- $p$: success probability in each single Bernoulli experiment.

### Definition

A negative binomial random variable $X$ with parameters $r\in\mathbb{N} \wedge p\in(0, 1)$ has range $\mathbb{N}_{\ge r} := \{r, r + 1, ... \}$. It is defined by a p.m.f. of the form:

$$\mathbb{P}(X = k) = \binom{k - 1}{r - 1} p^r (1 − p)^{k - r} \text{ for } k = r, r + 1, ...$$

We write $X \sim \text{NegBin}(r, p)$

### Attributes

| **Attribute** | **Value**                                                      |
| ------------- | -------------------------------------------------------------- |
| Range         | $\mathbb{N}_{\ge r}$                                           |
| Parameters    | $r\in\mathbb{N}\wedge p\in(0,1)$                               |
| Notation      | $X \sim \text{NegBin}(r, p)$                                   |
| P.m.f.        | $\mathbb{P}(X = k) = \binom{k - 1}{r - 1} p^r (1 − p)^{k - r}$ |
| Mean          | $\mathbb{E}[X] = { r \over p }$                                |
| Variance      | $Var(X) = r \cdot { 1 - p \over p^2 }$                         |

## Hypergeometric Distribution

### Interpretation

The hypergeometric distribution $\text{Hypgeo}(N, k, n)$ models the number of successes in $n$ draws without replacement from a set of $N$ objects in total, out of which $k$ are classified as “success”.

Parameters:

- $N$: size of the population.
- $n$: size of the sample.
- $k$: number of “success” individuals within the population.

### Definition

A Hypergeometric random variable $X$ with parameters $N\in\mathbb{N}_0\wedge k, n ∈ {0, . . . , N}$
has range $\{max(\{ 0, n + k - N \}), ..., min(\{ n, k \}) \}$. It is defined by a p.m.f. of the form:

$$\mathbb{P}(X = i) = { \binom{k}{i}\binom{N-k}{n-i}\over\binom{N}{n} }$$

We write $X \sim \text{Hypgeo}(N, k, n)$.

### Attributes

| **Attribute** | **Value**                                                                     |
| ------------- | ----------------------------------------------------------------------------- |
| Range         | $\{max(\{ 0, n + k - N \}), ..., min(\{ n, k \}) \}$                          |
| Parameters    | $N\in\mathbb{N}_0\wedge k, n ∈ {0, . . . , N}$                                |
| Notation      | $X \sim \text{Hypgeo}(N, k, n)$                                               |
| P.m.f.        | $\mathbb{P}(X = i) = \binom{k}{i}\cdot\binom{N-k}{n-i}\cdot\binom{N}{n}^{-1}$ |
| Mean          | $\mathbb{E}[X] = n\cdot{k\over N}$                                            |
| Variance      | $Var(X) = n{k\over N}(1-{k\over N}){N-n \over N-1}                            |

## Poisson random variable

### Interpretation

The Poisson distribution $\text{Poi}(\lambda)$ models the number of occurrences of a rare event in a given time-interval or spatial area.

Parameters:

- $\lambda$: average number of times the event happens in a given interval / spatial area.

### Definition

A Poisson random variable $X$ with parameter $\lambda > 0$ has range $\mathbb{N}_0$. It is defined by a p.m.f. of the form:

$$\mathbb{P}(X = k) = { e^{-\lambda}\cdot\lambda^k\over k!}\text{ for }k = 0, 1, 2, ...$$

We write $X \sim \text{Poi}(\lambda)$.

### Attributes

| **Attribute** | **Value**                                                                                |
| ------------- | ---------------------------------------------------------------------------------------- |
| Range         | $\mathbb{N}_0$                                                                           |
| Parameters    | $\lambda > 0$                                                                            |
| Notation      | $X \sim \text{Poi}(\lambda)$                                                             |
| P.m.f.        | $\mathbb{P}(X = k) = e^{-\lambda}\cdot\lambda^k\cdot{1\over k!}\wedge k \in\mathbb{N}_0$ |
| Mean          | $\mathbb{E}[X] = \lambda$                                                                |
| Variance      | $Var(X) = \lambda$                                                                       |

