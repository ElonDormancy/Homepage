---
layout: cv-archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

<style>
a.uline {text-decoration:underline;}

</style>

{% include base_path %}



# Guangcheng Liu(Dormancy)

Bayi Road Wuhan Hubei P.R China

Email:[dormant@whu.edu.cn](mailto:dormant@whu.edu.cn)/[gchen_liu@163.com](mailto:gchen_liu@163.com)

# RESEARCH EXPERIENCES

*Quantum Information and Quantum Computing Seminar*

Learned the QCQI theory through different methods

+ Solved the rotation path problem on Bloch sphere via quaternion method

For example:

Exercise 4.15: (Composition of single qubit operations) The Bloch representation gives a nice way to visualize the effect of composing two rotations.
(1) Prove that if a rotation through an angle $\beta_{1}$ about the axis $\hat{n}_{1}$ is followed by a rotation through an angle $\beta_{2}$ about an axis $\hat{n}_{2}$, then the overall rotation is through an angle $\beta_{12}$ about an axis $\hat{n}_{12}$ given by
$$
\begin{aligned}
c_{12} &=c_{1} c_{2}-s_{1} s_{2} \hat{n}_{1} \cdot \hat{n}_{2} \\
s_{12} \hat{n}_{12} &=s_{1} c_{2} \hat{n}_{1}+c_{1} s_{2} \hat{n}_{2}-s_{1} s_{2} \hat{n}_{2} \times \hat{n}_{1}
\end{aligned}
$$
where $c_{i}=\cos \left(\beta_{i} / 2\right), s_{i}=\sin \left(\beta_{i} / 2\right), c_{12}=\cos \left(\beta_{12} / 2\right)$, and $s_{12}=\sin \left(\beta_{12} / 2\right)$.
(2) Show that if $\beta_{1}=\beta_{2}$ and $\hat{n}_{1}=\hat{z}$ these equations simplify to
$$
\begin{aligned}
c_{12} &=c^{2}-s^{2} \hat{z} \cdot \hat{n}_{2} \\
s_{12} \hat{n}_{12} &=s c\left(\hat{z}+\hat{n}_{2}\right)-s^{2} \hat{n}_{2} \times \hat{z}
\end{aligned}
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

Then the final rotation is obtained
$$
\begin{equation}
    v'' = q_1q_2v(q_1q_2)^* =q_{net}vq_{net}^*
\end{equation}
$$
Graßmann Product($q_1 = [a,\mathbf{v}],q_2 = [e,\mathbf{u}]$)

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
finally we derive:
$$
\begin{equation}
\begin{aligned}
    &c_{12} = c_1c_2-s_1s_2\hat{n}_1\cdot \hat{n}_2\\
    &s_{12}\hat{n}_{12} = c_{1} s_{2} \hat{n}_{2}+s_{1} c_{2} \hat{n}_{1}-s_{1} s_{2} \hat{n}_{2} \times \hat{n}_{1}
\end{aligned}
\end{equation}
$$

---

*Experimental study of quantum information processing in the ion trap system*

Determined whether the ions($\ge2$) chain is "cold" from carrier transition and blue band transition

+ Derived the formula of population after carrier transition and blue band transition

+ Used Python programming to obtain the mean vibrational quantum number and Rabi frequency

Preparation of entangled state through Mølmer–Sørensen gate

+ Derived of the evolution of the density matrix of two ions and state occupation under the drive of red and blue detuned lasers via series expansion/phase space method
+ Used Python programming to obtain optimal fidelity and the minimum time for Mølmer–Sørensen gate

---

*Quantum Spin Systems and Quantum Computation(Simulation)*

Used Python and C++ programming to simulate the evolution process of electron spins in NMR system with large scale by using Chebyshev polynomial method

Developed a high-performance universal quantum simulator with MPI that can easily build quantum circuits and map them to various physical systems[such as NMR,Ion Trap,Superconducting and so on]

Designed a Javascript program to make it extremely easy to build quantum circuits and simulate universal quantum circuit

# **SKILLS**

Atomic and optical physics experimental skills

Programming skills: C,C++,Javascript,Python,Lisp(20k+)

# Education

**School of Physics and Technology,Wuhan University,Wuhan,Hubei China**    *2019.9-2023.7(Expected)*

Tianjuan Class,a joint training class of the School of Physics of WHU and the WIPM of CAS.

**GPA**     3.85/4.0 (major) 3.87/4.0(total)

# CV

<a href="../files/cv.pdf" class="uline" style = "font-size:20px">Click Here For a Full Pdf Copy of My Curriculum Vitae</a>

