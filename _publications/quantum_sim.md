---
title: "Quantum Dynamics"
collection: publications
permalink: /publications/quantum_sim
excerpt: "Numerical solution of PDE with high performance method"
date: 2021.4
venue: 'COMPUTATIONAL PHYSICS GROUP(lead by Prof. Shengjun Yuan)'
classes: wide
---

## Numerical solution of $i\hbar \partial \psi = \hat{H}\psi$

The key to solving such problems is how to decompose $\exp(\hat{H}t)$(When the dimension of H is very large, the method of exact diagonalization is not so suitable)



When I first glance this equation, my first intuition is to use Taylor series expansion,when the time step $\tau$ is small.



$$
\hat{U}(\tau) = I+\tau H
$$



However, such a decomposition will result in the operator that is not unitary.



Thus *Crank–Nicolson method*  may be a good method,which guarantee the operator is unitary.



Nowadays he most common method used to solve the equation is **Trotter-Suzuki Formula**.Its main idea to decompose the exponential formula is making use of **Lie-Trotter-Suzuki Time Integration**



$$
\exp(t(H_1+\cdots+H_p)) = \lim_{m\to\infty}(\prod_{i=1}^{p} \exp(tH_i/m))^m
$$



where $H = \sum_{i=1}^{p}H_i$



Because this method is very commonly used in quantum simulations.



In superconducting circuit

<center>    <img  src="/Homepage/images/Quantum_Simulation/simulation_2.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Han J, Cai W, Hu L, et al.Physical Review Letters, 2021, 127(2): 020504.</div> </center>

In Ion Trap

<center>    <img src="/Homepage/images/Quantum_Simulation/simulation_1.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Hempel, Cornelius.Diss. 2014.</div> </center>

We use this method to simulate the propagation of electromagnetic waves in TM Mode

<center>    <img src="/Homepage/images/Quantum_Simulation/Maxwell_Wave.gif">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">TM Mode Demo</div> </center>

And Chebyshev Time Integration may also solve the problem fastly


$$
\exp(tH) = [J_0(z)I+2\sum_{n=1}^{+\infty}J_n(z)i^n T_n(B)]
$$

<center>    <img src="/Homepage/images/Quantum_Simulation/Schrodinger.gif" width = "60%">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">The result of numerically solving the Schrödinger equation and its initial state is a Gaussian Wave(Grid)</div> </center>