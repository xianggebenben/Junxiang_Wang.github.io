---
title: "Nonconvex Generalization of Alternating Direction Method of Multipliers(ADMM)"
excerpt:
collection: portfolio
---

Due to the advantages and popularity of non-differentiable regularized and distributive computing for complex optimization problems, the Alternating Direction Method of Multipliers (ADMM) has received a great deal of attention in recent years. The standard ADMM was originally proposed to solve the following separable convex optimization problem:

$$\min_{x,z} f(x)+g(z)\ \ \ s.t. \ Ax+Bz=c.$$

where $f(x)$ and $g(z)$ are closed convex functions, $A$ and $B$ are matrices and $c$ is a vector. The Augmented Lagrangian function is formulated as follows:$L_\rho(x,z,y)=f(x)+g(z)+y^T(Ax+Bz-c)+(\rho/2)\Vert Ax+Bz-c\Vert^2_2$, where $\rho>0$ is a tuning parameter to control the quadratic penalty $\Vert Ax+Bz-c\Vert^2_2$, and $y$ is a dual variable. The ADMM works in the following fashion:

$$\begin{align}
&\nonumber x^{k+1}\leftarrow \arg\min_x L_\rho(x,z^k,y^k).\\\nonumber
&z^{k+1}\leftarrow \arg\min_z L_\rho(x^{k+1},z,y^k).\\\nonumber
&y^{k+1}\leftarrow y^k+\rho(Ax^{k+1}+Bz^{k+1}-c).
\end{align}$$

For more information, please refer to Boyd's [tutorial paper](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://stanford.edu/~boyd/papers/pdf/admm_distr_stats.pdf).

While the ADMM has been extensively applied in the convex problems, its extension on the nonconvex problems are not well-studied. This motivates me to explore two different nonconvex problems addressed by ADMM.

**1.The Nonlinear-Equality-Constrained Problem.** This problem can be formulated as follows:

$$\min_{x_1,x_2} \ F_1(x_1)+F_2(x_2) \ s.t. \ f_1(x_1)+f_2(x_2)=0 $$

where $F_1(x_1)$ and $F_2(x_2)$  are proper continuous functions, and $f_1:\mathbb{R}^{m_1}\rightarrow \mathbb{R}^{d}$ and $f_2:\mathbb{R}^{m_2}\rightarrow \mathbb{R}^{d}$ can be nonlinear. This problem has a wide range of applications such as 1-bit compressive sensing and multi-instance learning. It is investigated in my following paper:

**Junxiang Wang** and Liang Zhao. Nonconvex Generalization of Alternating Direction Method of Multipliers for Nonlinear Equality Constrained Problems. Results in Control and Optimization, 2021. [paper](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/RICO2021/neADMM.pdf) [code](https://github.com/xianggebenben/neADMM)

In this paper, we extend the ADMM naturally to nonlinear equality-constrained problems, called neADMM. The difficulty of neADMM is to solve nonconvex subproblems. We provide globally optimal solutions to them in two important applications.

**2.The Multi-convex Problem.** This problem can be formulated as follows:

$$\min\nolimits_{x_1,\cdots,x_n,z} f(x_1,\cdots,x_n)\!+h(z)\ \ \  s.t. \sum_{i=1}^n A_i x_i-z=0.$$

where $x_i\in \mathbb{R}^{p_i}(i=1,\cdots,n)$, $z\in \mathbb{R}^{q}$, $f(x_1,\cdots,x_n): \mathbb{R}^p\rightarrow \mathbb{R}\cup\{\infty\}(p=\sum\nolimits_{i=1}^n p_i)$ are proper, continuous, multi-convex and possibly nonsmooth functions, $h(z)$ is a proper, differentiable and convex function. $A_i\in \mathbb{R}^{q\times p_i}(i=1,\cdots,n)$ are matrices. This problem covers a board range of applications such as multi-task learning and social media mining. It is investigaed in my following paper:

**Junxiang Wang** and Liang Zhao. Convergence and Applications of ADMM on the Multi-convex Problems. 26th Pacific-Asia Conference on Knowledge Discovery and Data Mining (PAKDD 2022), (acceptance rate: 19.3%), Chengdu, China, May 2022. [paper](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/PAKDD2022/multi_convex_ADMM.pdf) [code](https://github.com/xianggebenben/miADMM) [slides](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/PAKDD2022/PAKDD_2022.pdf)

In this paper, we propose a generic ADMM framework with multiple coupled variables in both objective and constraints. Convergence to a Nash point is proven with a sublinear convergence rate $o(1/k)$. Two important applications are discussed as special cases under our proposed ADMM framework.
