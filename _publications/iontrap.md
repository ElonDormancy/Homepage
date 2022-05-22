---
title: "Ion Trap System"
collection: publications
permalink: /publications/iontrap
excerpt: "Experimental study of quantum information processing in the ion trap system"
date: 2022.5
venue: 'APM'
classes: wide
---
# Experimental study of quantum information processing in the ion trap system

Single ion's dynamics is dicussed detailed in [1]

<center><img  src="/Homepage/images/Ion_Trap_System/two_ions_trap.png">    <br>    <div style="color:orange; border-bottom: 1px solid #d9d9d9;    display: inline-block;    color: #999;    padding: 2px;">Two Trapped Ions</div> </center>

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

