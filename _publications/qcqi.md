---
title: "Quantum Information and Quantum Computing Seminar"
collection: publications
permalink: /publications/qcqi
excerpt: "Learned the QCQI theory through different methods"
date: 2021.7
venue: 'University of Science and Technology of China(USTC)'
classes: wide
---


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

More details of the Seminar are available on [QCQI Summary](https://zhuanlan.zhihu.com/p/395208248)
