---

layout: archive
title: "Work"
permalink: /publications/
author_profile: true
classes: wide
---

Details of Research Experience

[toc]

# Quantum Information and Quantum Computing Seminar

> Through this seminar, I master almost every detail of the QCQI[1] and have a deep discussion with my classmates for each chapter and exercise.

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

> [1] Nielsen M A, Chuang I. Quantum computation and quantum information[J]. 2002.

# Experimental study of quantum information processing in the ion trap system

Single ion's dynamics is dicussed detailed in [1]

<center>    <img  src="/Homepage/images/Ion_Trap_System/two_ions_trap.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Two Trapped Ions</div> </center>

## Whether the ions chain is “cold”

After sideband cooling,the population will oscillate with the following formula:[2]



$$
P_{S} = \frac{1}{2}(1+\sum_{n}p_n\cos(\Omega_{s+n,n}t))
$$



$$
P_{D} = \frac{1}{2}(1-\sum_{n}p_n\cos(\Omega_{s+n,n}t))
$$



where $p_n = \frac{1}{\bar{n}+1}(\frac{\bar{n}}{\bar{n}+1})^n$,$s=1\rightarrow$blueband transition($\Omega_{n+1,n}=\eta\sqrt{n+1}\Omega_0$),$s=0\rightarrow$carrier transition($\Omega_{n,n}\approx\Omega_0(1-\eta^2n)$)



<center>    <img  src="/Homepage/images/Ion_Trap_System/heating_rate.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">The mean vibrational mode is obtained by fitting the above formula</div> </center>



Thus we can easily obtain the heating rate:

<center>    <img  src="/Homepage/images/Ion_Trap_System/heating_rates.png"  width="60%">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Heating Rate</div> </center>

Thus based on the fitting formula above,we are able to obtain whether the ions chain is "cold".



Because the two ions are so close that the laser will irradiate the two ions directly.The population is:$P_{D\cdots D} = P_D^n$



And fitting result will show below:



<center>    <img  src="/Homepage/images/Ion_Trap_System/Two_Ions.jpg" width="60%">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Two Ions</div> </center>



And we are able to get the mean vibrational mode to evaluate whether the ion chains are "cold"

## Mølmer-Sørensen Gate

The Mølmer–Sørensen gate is a two qubit gate,which is able to realize the preparation of entangled states without addressing the single ion.[3,4,5]



I have derived the dynamics of MS by means of series expansion and phase space and obtained the same results.



Further,based on the time evolution operator:



$$
U(t) = \hat{D}(\alpha(t)S_{y,\psi})\exp(i(\lambda t-\chi \sin(\epsilon t)S^2_{y,\psi} ))
$$



where $\psi = \frac{4\Omega}{\delta}\sin(\zeta)$



when $\zeta=0$



<center>    <img  src="/Homepage/images/Ion_Trap_System/ms_n=0.jpg" width="60%">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">n=0</div> </center>

<center>    <img  src="/Homepage/images/Ion_Trap_System/ms_n=20.jpg" width="60%">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">n=20</div> </center>



I propose a simpler numerical method to simulate this dynamics process and can be extended to more ions.

The numerical result:

<center>    <img  src="/Homepage/images/Ion_Trap_System/num_res_n=0.jpg" width="60%">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">n=0</div> </center>

<center>    <img  src="/Homepage/images/Ion_Trap_System/num_res_n=20.jpg" width="60%">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">n=20</div> </center>

The result almost the same.

In the experiment the exact value of $\zeta$ is not easily controlled,the  numerical method will allow you to vary $\zeta$.



A light field resonant with the transition will not only drive Rabi oscillations on this transition.But also off-resonantly drive the carrier transition.



<center>    <img  src="/Homepage/images/Ion_Trap_System/ms_c_n=0.jpg" width="60%">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">n=0(Carrier Transition)</div> </center>



Amplitude pulse shaping to suppress carrier transitions[6,7]:

<center>    <img  src="/Homepage/images/Ion_Trap_System/suppres_c.jpg">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Simulated time evolution for the system initially in the ground state for a Rabi frequency</div> </center>



Blackman window shaping are able to suppress carrier transitions very well

> [1] Leibfried, Dietrich, et al. "Quantum dynamics of single trapped ions." *Reviews of Modern Physics* 75.1 (2003): 281.
>
> [2] Hempel C. Digital quantum simulation, Schrödinger cat state spectroscopy and setting up a linear ion trap[D]. , 2014.
>
> [3] Roos C F. Ion trap quantum gates with amplitude-modulated laser beams[J]. New Journal of Physics, 2008, 10(1): 013002.
>
> [4] Kirchmair G, Benhelm J, Zähringer F, et al. Deterministic entanglement of ions in thermal states of motion[J]. New Journal of Physics, 2009, 11(2): 023002.
>
> [5] Shapira Y, Shaniv R, Manovitz T, et al. Robust entanglement gates for trapped-ion qubits[J]. Physical review letters, 2018, 121(18): 180502.
>
> [6] Kirchmair, Gerhard. *Quantum non-demolition measurements and quantum simulation*. na, 2010. 
>
> [7] Schindler, Philipp. *Frequency synthesis and pulse shaping for quantum information processing with trapped ions*. na, 2008.



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

"UQCS" is a visualized universial quantum circuits[1,2] makes it extremely easy to build quantum circuits,intended to help people in about construct quantum circuits.



When the number of qubits more than 12,"UQCS" will act as a kit to plot quantum circuit,which then are able to be exported to our own compiler to compile.And you have ability to get everything about the circuit(for example the sketch figure of the circuit with $\LaTeX$ code )



Input area:



<center>    <img  src="/Homepage/images/UQCS/uqc.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">DRAG AREA</div> </center>



Group mode works when you want to move some quantum gate collectively.

> The control gate will in the same group automatically.



We provide two form of result:



[Density Matrix](https://en.wikipedia.org/wiki/Density_matrix)



Projection Probability:Take the inner product of each basis vector and the final evolved state.



Output area



<center>    <img  src="/Homepage/images/UQCS/uqcoutput.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">OUTPUT</div> </center>



More details:



[Quantum Simulator](https://github.com/ElonDormancy/QuantumSimulator)



The method of simulation can be found in [3]



> [1] https://github.com/Strilanc/Quirk
>
> [2] https://github.com/stewdio/q.js
>
> [3] De Raedt, Hans, and K. Michielsen. "Computational methods for simulating quantum computers." *arXiv preprint quant-ph/0406210* (2004).



## Simulation in spin chain system

Hamiltonian of a spin ½ system with N coupled spins:



$$
H(t)=-\sum_{i, j=1}^{N} \sum_{\alpha=x, y, z} J_{i, j}^{\alpha}(t) S_{i}^{\alpha} S_{j}^{\alpha}-\sum_{i, j=1}^{N} \sum_{\alpha=x, y, z} h_{i}^{\alpha}(t) S_{i}^{\alpha}
$$



And Chebyshev Time Integration can solve the problem fastly:


$$
\exp(tH) = [J_0(z)I+2\sum_{n=1}^{+\infty}J_n(z)i^n T_n(B)]
$$

Example:



<center>    <img  src="/Homepage/images/Ising_Model_Spins.gif">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Ising-like Model</div> </center>	

<center>    <img  src="/Homepage/images/Heisenberg_Model_Spins.gif">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Heisenberg Model</div> </center>	

From the method below we can simulate a large scale spin system

## NMR Quantum Simulator

Nuclear spin systems would be nearly ideal for quantum computation if only spin-spin couplings could be large and controllable.[1,2,3]

We will follow the step that the experiment do, and in the simulator, you can own your virtual NMR quantum simulator

### Initialization

Let's begin with the thermal state:


$$
\rho_{\text{th}} = \frac{e^{-\beta \hat{H}}}{Z}
$$



In our simulator we can easily get the thermal state:($-2^{-n}I$)

<center>    <img  src="/Homepage/images/NMR_Quantum_Simulator/Thermal_State.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Thermal State</div> </center>	

Because of the difficulty in preparing pure spin states in NMR systems, almost all NMR quantum information processing experiments have used pseudo-pure states(PPS)

> Method:1.Temporal averaging 2.Spatial averaging

A pseudo-pure state in a system of n spins is simply a mixed state of the form:


$$
\text{PPS} = \frac{1}{2^n}(1-\epsilon)I+\epsilon|\psi\rangle \langle \psi|
$$


And the sample we "use" is $CHCl_3$ which is a two qubit sample. Its related parameters are listed below[4]

|          | $C_{13}$ | $H_1$ | $T_1$ | $T_2$ |
| :------: | -------- | ----- | ----- | ----- |
| $C_{13}$ | 500M     | 215   | 18.8s | 0.35s |
| $H_{1}$  | 215      | 125M  | 10.9s | 3.3s  |

And the Hamiltonian in the $B_0$(z direction) is:



$$
\mathsf{H}_0 = \sum_{i}\hbar\pi w_i \sigma_z^i+\sum_{i<k ,=1}\frac{\pi}{2}\hbar J_{ik}\sigma_z^i\sigma_z^k
$$

And the control hamiltonian is:



$$
\mathsf{H}_{\text{rf}} = \sum_i^n -\hbar \gamma_i B_1[\cos(w_{\text{rf}}t+\phi))\sigma_x+\sin(w_{\text{rf}}t+\phi))\sigma_y
$$



The initial state is:$|00\rangle$



<center>    <img  src="/Homepage/images/NMR_Quantum_Simulator/rho0.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Initial State(00)</div> </center>	

We can control the control hamiltonian to realize the single qubit gate and control gate

### Single Qubit Gate

For example ($R_x(\frac{\pi}{2})$)





<center>    <img  src="/Homepage/images/NMR_Quantum_Simulator/rx1.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">X</div> </center>	



### Control Gate

And also we can make use of J-J couple to realize the control gate:



The inital state set below is $|10\rangle$



<center>    <img  src="/Homepage/images/NMR_Quantum_Simulator/cnot1c2.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">CNOT</div> </center>	

### Noise

We use kraus sum operation[5]



$$
\varepsilon(\rho) \rightarrow \sum_k E_k \rho E_k^\dagger
$$



And the operator $E_k$ is closely related to $T_1,T_2$,The room temperature

We can use this model to simulate the decoherence process

<center>    <img  src="/Homepage/images/NMR_Quantum_Simulator/decoherence.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Decoherence process</div> </center>	

Up to now we can simulate the nmr quantum computation process

> [1] Jones, Jonathan A. "Quantum computing with NMR." *arXiv preprint arXiv:1011.1382* (2010).
>
> [2] Vandersypen L M K, Chuang I L. NMR techniques for quantum control and computation[J]. Reviews of modern physics, 2005, 76(4): 1037.
>
> [3] Oliveira I, Sarthour Jr R, Bonagamba T, et al. NMR quantum information processing[M]. Elsevier, 2011.
>
> [4] Chuang, Isaac L., et al. "Experimental realization of a quantum algorithm." *Nature* 393.6681 (1998): 143-146.
>
> [5] Vandersypen L M K, Steffen M, Breyta G, et al. Experimental realization of Shor's quantum factoring algorithm using nuclear magnetic resonance[J]. Nature, 2001, 414(6866): 883-887.

