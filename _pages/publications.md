---

layout: archive
title: "Work"
permalink: /publications/
author_profile: true
classes: wide
---

Details of Research Experience

# Quantum Information and Quantum Computing Seminar

> Through this seminar I master almost every detail of the QCQI and have a deep discussion with my classmates for each chapter and exercise.

***Exercise 4.15: (Composition of single qubit operations) The Bloch representation gives a nice way to visualize the effect of composing two rotations.***

> Here is an example of using quaternions to solve a question in QCQI, the proof will be complicated by the Rodrigues' rotation formula, while using quaternions everything will become very obvious.
>
> **Rodrigues' rotation formula:**
>
> 
> $$
> \begin{equation}
> \vec{v}_{\text{rot}} = \vec{v}\cos\theta+(\vec{k}\times \vec{v})\sin \theta+\vec{k}(\vec{k}\cdot\vec{v})(1-\cos\theta)
> \end{equation}
> $$
> 
>
> where $\vec{k}$ is a unit vector describing an axis of rotation about which $\vec{v}$ rotates by an angle $\theta$ according to the right hand rule



(1) Prove that if a rotation through an angle $\beta_{1}$ about the axis $n_1$ is followed by a rotation through an angle $\beta_{2}$ about an axis $n_2$, then the overall rotation is through an angle $\beta_{12}$ about an axis $n_{12}$ given by

$$
\begin{equation}
c_{12} =c_{1} c_{2}-s_{1} s_{2} \hat{n}_{1} \cdot \hat{n}_{2}
\end{equation}
$$
$$
s_{12} \hat{n}_{12} =s_{1} c_{2} \hat{n}_{1}+c_{1} s_{2} \hat{n}_{2}-s_{1} s_{2} \hat{n}_{2} \times \hat{n}_{1}
$$



where $c_{i}=\cos(\beta_{i} / 2), s_{i}=\sin (\beta_{i} / 2), c_{12}=\cos (\beta_{12} / 2)$, and $s_{12}=\sin (\beta_{12} / 2)$.



(2) Show that if $\beta_{1}=\beta_{2}$ and $\hat{n}_{1}=\hat{z}$ these equations simplify to

$$
\begin{equation}
c_{12} =c^{2}-s^{2} \hat{z} \cdot \hat{n}_{2}
\end{equation}
$$
$$
s_{12} \hat{n}_{12} =s c\left(\hat{z}+\hat{n}_{2}\right)-s^{2} \hat{n}_{2} \times \hat{z}
$$



where $c=c_{1}$ and $s=s_{1}$.



First rotate the angle $\beta_2$ around $\hat{n}_2$ and then rotate the angle $\beta_1$ around $\hat{n}_1$, then the corresponding quaternion is:


$$
\begin{equation}
    q_2 = [cos\frac{\beta_2}{2},sin\frac{\beta_2}{2}\hat{n}_2]
\end{equation}
$$

$$
\begin{equation}
    q_1 = [cos\frac{\beta_1}{2},sin\frac{\beta_1}{2}\hat{n}_1]
\end{equation}
$$

Then the final rotation result is obtained


$$
\begin{equation}
    v'' = q_1q_2v(q_1q_2)^* =q_{net}vq_{net}^*
\end{equation}
$$



Graßmann Product$q_1 = [a,\mathbf{v}],q_2 = [e,\mathbf{u}]$


$$
\begin{equation}
    q_{net} = q_1q_2 = [ae-\mathbf{v}\cdot \mathbf{u},a\mathbf{u}+e\mathbf{v}+\mathbf{v}\times \mathbf{u}]
\end{equation}
$$



Thus:


$$
\begin{equation}
    q_{net} = [c_1c_2-s_1s_2\hat{n}_1\cdot \hat{n}_2,c_{1} s_{2} \hat{n}_{2}+s_{1} c_{2} \hat{n}_{1}+s_{1} s_{2} \hat{n}_{1} \times \hat{n}_{2}]
\end{equation}
$$



then we get the result:


$$
\begin{equation}
    c_{12} = c_1c_2-s_1s_2\hat{n}_1\cdot \hat{n}_2
\end{equation}
$$

$$
    s_{12}\hat{n}_{12} = c_{1} s_{2} \hat{n}_{2}+s_{1} c_{2} \hat{n}_{1}-s_{1} s_{2} \hat{n}_{2} \times \hat{n}_{1}
$$



# Experimental study of quantum information processing in the ion trap system



# Quantum Spin Systems and QuantumComputation(Simulation)

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

<center>    <img  src="/Homepage/images/simulation_2.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Han J, Cai W, Hu L, et al.Physical Review Letters, 2021, 127(2): 020504.</div> </center>

In Ion Trap

<center>    <img src="/Homepage/images/simulation_1.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Hempel, Cornelius.Diss. 2014.</div> </center>

We use this method to simulate the propagation of electromagnetic waves in TM Mode

<center>    <img src="/Homepage/images/Maxwell_Wave.gif">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">TM Mode Demo</div> </center>

And Chebyshev Time Integration may also solve the problem fastly


$$
\exp(tH) = [J_0(z)I+2\sum_{n=1}^{+\infty}J_n(z)i^n T_n(B)]
$$

<center>    <img src="/Homepage/images/Schrodinger.gif">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">The result of numerically solving the Schrödinger equation and its initial state is a Gaussian Wave(Grid)</div> </center>



## Universal Quantum Circuit Simulator

"易(Yi)" is a visualized universial quantum circuits[The limit on the number of qubits is 12] makes it extremely easy to build quantum circuits,intended to help people in about construct quantum circuits.



When the number of qubits more than 12,"易" will act as a kit to plot quantum circuit,which then are able to be exported to, for example, [Qiskit](https://www.qiskit.org/) or our own compiler to compile.



Input area:



<center>    <img  src="/Homepage/images/uqc.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">DRAG AREA</div> </center>



Group mode works when you want to move some quantum gate collectively.

> The control gate will in the same group automatically.



We provide two form of result:



[Density Matrix](https://en.wikipedia.org/wiki/Density_matrix)



Projection Probability:Take the inner product of each basis vector and the final evolved state.



Output area



<center>    <img  src="/Homepage/images/uqcoutput.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">OUTPUT</div> </center>



More details:



[Quantum Simulator](https://github.com/ElonDormancy/QuantumSimulator)



