# Lecture 5

This lecture is about continuous distributions, much like [lecture 3](./lecture-03.md) but those were discreet distributions.

## Uniform Continuous Distribution

### Definition

A continuous random variable $X$ with distribution $\text{Unif}([0, 1])$ is called a
standard uniform random variable.

### Transformations

If $X \sim \text{Unif}([0, 1])$ and $a < b$, then you can transform to $Y := (b − a) \cdot X + a \sim \text{Unif}([a, b])$. The other way around is also possible: let $Y \sim \text{Unif}([a, b]) for a < b, then $X := { Y - a \over b - a } \sim \text{Unif}([0, 1])$.

### Attributes

| **Attribute** | **Value**                                             |
| ------------- | ----------------------------------------------------- |
| Range         | $[a, b]$                                              |
| Parameters    | $a, b \in \mathbb{R}$                                 |
| Notation      | $X \sim \text{Unif}([a, b])$                          |
| P.d.f.        | $f_X(x) = {1 \over b - a}$ for $a\ge x\ge b$ else $0$ |
| Mean          | $\mathbb{E}[X] = { 1 \over 2} a + { 1 \over 2} b$     |
| Variance      | $Var(X) = (b- a)^2 \cdot { 1 \over 12}$               |

## Normal distribution 

### Interpretation

The normal distribution models random quantities that are composed of many small & independent influences.

### Definition

A continuous random variable $X$ is normally distributed with parameters $\mu\in\mathbb{R}$ and $\sigma^2>0$, if its p.d.f. is given by

$$f_X (x) = { 1 \over \sigma\sqrt{2\pi} } \cdot \exp({ - {(x - \mu)^2 \over 2\sigma^2} })\text{ for }x\in\mathbb{R} \text{ where } \exp(x) = e^x$$

We write $X \sim \mathcal{N} (\mu, \sigma^2)$.

### Transformation

For $X \sim \mathcal{N}(\mu, \sigma^2)$ and $x\in\mathbb{R}$:

$$\mathbb{P}(X \le x) = \Phi\bigg({ x - \mu \over \sigma }\bigg)$$

Fix $z\in\mathbb{R}$. Choosing $x = \sigma z + \mu$ in the last identity,

$$\mathbb{P}\bigg({ X - \mu \over \sigma } \le z \bigg) = \mathbb{P}(X\le x) = \Phi\bigg({ x - \mu \over \sigma }\bigg) = \Phi(z)$$

### Standard Normal Distribution

A continuous random variable $Z \sim \mathcal{N}(0, 1)$ is said to have a standard normal distribution. 

$Z \sim \mathcal{N} (0, 1)$ has p.d.f.

$$\phi(z) = f_Z(z) = { 1 \over \sqrt{2\pi} } \cdot \exp({ -{z^2 \over 2} }) \text{ where } \exp(x) = e^x$$

and has c.d.f.: 

$$\Phi(z) = \mathbb{P}(Z \le z ) = \int^z_{-\infty} { 1 \over \sqrt{2\pi} } \exp({ -{ t^2 \over 2 } }) dt \text{ where } \exp(x) = e^x$$

#### Symmetries

The normal p.d.f. is symmetric with respect to $\mu$: If $X\sim\mathcal{N}(\mu, \sigma^2), then

$$\forall_a : f_X (\mu - a) = f_X (\mu + a)$$

Moreover

$$\forall_a : F_X (\mu - a) = \mathbb{P}(X \le\mu - a) = P(X \ge \mu + a) = 1 - F_X (\mu + a)$$

Special case: If $Z \sim\mathcal{N}(0, 1), then \forall_z:

$$\phi(-z) = 1 - \phi(z)$$

### Attributes

| **Attribute** | **Value**                                                                                 |
| ------------- | ----------------------------------------------------------------------------------------- |
| Range         | $(-\infty, \infty)$                                                                       |
| Parameters    | $\mu\in\mathbb{R}, \sigma^2 > 0$                                                          |
| Notation      | $X \sim \mathcal{N}(\mu, \sigma^2)$                                                       |
| P.d.f.        | $f_X (x) = { 1 \over \sigma\sqrt{2\pi} } \cdot \exp({ - {(x - \mu)^2 \over 2\sigma^2} })$ |
| Mean          | $\mathbb{E}[X] = \mu$                                                                     |
| Variance      | $Var(X) = \sigma^2$                                                                       |

## Stochastic process

### Definition 

A stochastic process is a collection of random variables $(X_t)_{t\in\mathcal{T}}$ indexed by a
time variable $t\in\mathcal{T}$.

## Poisson Process

### Interpretation

The following is a process version to the Poisson distribution. It keeps track of the number of events in all potential time intervals $[0, t]$ simultaneously.

### Properties

Any Poisson process satisfies the following properties:

1. The number of events within each interval $[s, t]$ follows a Poisson distribution with parameter $\lambda(t - s)$. In particular, the distribution only depends on the length of the given interval.
2. The numbers of events in disjoint intervals are independent random variables.

### Definition

For any $t \ge 0$, let $N(t)$ denote the number of events that have occurred in the interval $[0, t]$. Let $\lambda > 0$ denote the average number of events that occur in $[0, 1]$. The collection of random variables $\big(N(t)\big)_{t\ge 0}$ is then called a Poisson process with rate $\lambda > 0$.

### Attributes


| **Attribute** | **Value**                                                                                        |
| ------------- | ------------------------------------------------------------------------------------------------ |
| Range         | $N(t) \in \mathbb{N}_0 = \{ 0, 1, 2, \dots \}$ for each $t \ge 0$                                |
| Parameters    | $\lambda > 0$ (rate)                                                                             |
| Notation      | $(N(t))_{t \ge 0} \sim \text{Poi}(\lambda\cdot t)$                                               |
| P.m.f.        | $\mathbb{P}(N(t)=k) = (\lambda t)^k { 1 \over k! } \exp({-\lambda t}), \quad k \in \mathbb{N}_0$ |
| Mean          | $\mathbb{E}\big[N(t)\big] = \lambda t$                                                           |
| Variance      | $\mathrm{Var}(N(t)) = \lambda t$                                                                 |

## Exponential Distribution 

### Interpretation

The exponential distribution is commonly used to model waiting times (in a Poisson process).

Parameters:
- $\lambda$: is the frequency of the given event per time unit (in the Poisson process).

### Definition

A continuous random variable $X$ has an exponential distribution with parameter $\lambda > 0$, if its p.d.f. $f_X$ is given by

$$f_X(x) = \begin{cases} \lambda\cdot\exp(-\lambda\cdot x) & \text{if } x \ge 0 \text{ where } \exp(x) = e^x, \\ 0 & \text{otherwise}\end{cases}$$

We write $X \sim\text{Exp}(\lambda)$.

### Attributes

| **Attribute**       | **Value**                                                                  |
| ------------------- | -------------------------------------------------------------------------- |
| Range               | $[0, \infty)$                                                              |
| Parameters          | $\lambda > 0$ (rate)                                                       |
| Notation            | $X \sim \text{Exp}(\lambda)$                                               |
| P.d.f.              | $f_X(x) = \lambda\cdot\exp(-\lambda x)$ for $x \ge 0$ where $exp(x) = e^x$ |
| Mean                | $\mathbb{E}[X] = \frac{1}{\lambda}$                                        |
| Variance            | $\mathrm{Var}(X) = \frac{1}{\lambda^2}$                                    |
| Memoryless property | $\mathbb{P}(X > s+t \mid X > s) = \mathbb{P}(X > t)$                       |
