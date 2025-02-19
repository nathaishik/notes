---
title: The theory of Ideal Gas
layout: default
parent: Statistical Physics
---

# The theory of Ideal Gas

Now the title is a bit misleading, if I can be frank, but we are going to derive the ideal gas law from entropy.

<!-- Talk about entropy and multiplicity -->

## Background

### Concepts

**Entropy**, $S$ is the measure of the degree of randomness in a system. A state with higher number of degenerate arrangements, or higher multiplicity, has higher entropy.
$S$ is assumed to be a function of $U$, $V$, $N$ where $V$ is the volume and $N$ is the number of particles. So, $S = S(U, V, N)$. Differentiating:

$$ dS = \left(\frac{\partial S}{\partial U}\right)\_{V,N} dU + \left(\frac{\partial S}{\partial V}\right)\_{U,N}dV + \sum\_{j=1}^M \left(\frac{\partial S}{\partial N\_j}\right)\_{U,V,N\_{i \neq j}}dN\_j $$

Now, $(\partial S/\partial U)\_{V, N} = 1/T $, $ (\partial S/\partial V)\_{U, N} = p/T $, and $ (\partial S/\partial N)\_{U, V, N\_{i \neq j} } = -\mu_j/T $ , where $T$ is the temperature, $p$ is the pressure and $\mu_j$ is the chemical potential. These are measureable properties. So,

$$
dS = \frac{1}{T}dU + \frac{p}{T}dV - \sum_{j=1}^M \frac{\mu_j}{T}dN_j
$$

**Multiplicty** is represented by $W$. It is the count of the possible number of arrangements while satisfying specific conditions. For example, the multiplicity of a system with $M$ boxes and $N$ particles, given that each box can have only one particle, can be calculated as:
$$
W = {M \choose N} = \frac{M!}{N!(M-N)!}
$$

Entropy is given by $S = k\ln{(W)}$ where $k$ is the Boltzmann constant.

<!-- describe the model and what are the assumptions -->

### Model

To derive the ideal gas equation, we consider a gas with $N$ particles, encased in a container of volume V. The container has $M$ sites where the $N$ particles can go, each site accomodating only one particle at max. The position of one particle is not influenced by the other particles other than making a few potential sites unavailable for it to occupy. We also assume that $N \ll M$ which is reasonable given density of most gases are very low.

## Derivation

Let's start by calculating the multiplicity of the model described above.

### Calculating multiplicity

If $N$ particles are to be arranged in $M$ lattice sites, the multiplicity
$$
W = \frac{M!}{N!(M - N)!}
$$
Using sterling's approximation,
$$
W = \frac{M^M}{N^N (M - N)^{(M - N)}}
$$
So,
$$
\frac{S}{k} = M\ln{(M)} - N\ln{(N)} - (M - N)\ln{(M - N)}
$$

### The entropy equation

From the fundamental entropy equation,

$$
\frac{p}{T} = \left(\frac{\partial S}{\partial V}\right)
$$
$$
\frac{p}{T} = \left(\frac{\partial S}{\partial M}\right)_V \left(\frac{\partial V}{\partial M}\right)
$$

Now, 

$$
\left(\frac{\partial S}{\partial M}\right) = k\left[ 1 + \ln{(M)} - 1 - \ln{(M - N)} \right]
$$

$$
\left(\frac{\partial S}{\partial M}\right) = k\ln{\left(\frac{M}{M - N}\right)}
$$

$$
\left(\frac{\partial S}{\partial M}\right) = - k\ln{\left(1 - \frac{N}{M}\right)}
$$

Also, $(\partial M / \partial V) = 1/v_0 = (M / V)$ where $v_0$ is the volume per lattice.

### Combining

So,

$$
\frac{p}{T} = k \left(\frac{M}{V}\right)\ln{\left(1 - \frac{N}{M}\right)}
$$

Using the expansion of $\ln{(1 - x)} = - x/1 - x^2/2 - ...$
$$
\frac{p}{T} = - k \left(\frac{M}{V}\right)\left( - \frac{N}{M} - \frac{N}{2 M} - ... \right)
$$

For gases, $N \ll M$, so the higher order terms are negligible. Thus,
$$
\frac{p}{T} = - k \left(\frac{M}{V}\right)\left( - \frac{N}{M}\right)
$$

$$
\frac{p}{T} = k \left(\frac{M}{V}\right)\left(\frac{N}{M}\right)
$$

Thus, we have $\boxed{pV = NkT}$ which is the ideal gas equation for $N$ molecules of gas.

## Conclusion

Thus, the equation which was originally though to be an highly approximated and experimental one, is actually theoretically derivable.
