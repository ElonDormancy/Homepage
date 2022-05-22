---
title: "Universal Quantum Computer Simulator"
collection: publications
permalink: /publications/uqcs
excerpt: "universal quantum circuit simulation(including physical system)"
date: 2022.1
venue: 'COMPUTATIONAL PHYSICS GROUP(lead by Prof. Shengjun Yuan)'
classes: wide
---


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



<center>    <img  src="/Homepage/images/Quantum_Simulation/Ising_Model_Spins.gif">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Ising-like Model</div> </center>	

<center>    <img  src="/Homepage/images/Quantum_Simulation/Heisenberg_Model_Spins.gif">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Heisenberg Model</div> </center>	

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

<center><img  src="/Homepage/images/NMR_Quantum_Simulator/Thermal_State.png">    <br> <div style="width=40%;color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Thermal State</div> </center>	

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