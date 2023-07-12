---
title: "Deep Learning Optimization by Alternating Minimization"
excerpt:
collection: portfolio
---

Stochastic Gradient Descent (SGD) and its variants have gained popularity for training deep neural networks. However, theoretical guarantees on the convergence of SGD do not apply well to problems involving deep neural networks, which are nonsmooth and nonconvex. Additionally, SGD suffers from limitations such as the gradient vanishing problem, where the error signal diminishes during backpropagation, and sensitivity to poor conditioning, where small input changes lead to dramatic gradient changes. To address these drawbacks, Alternating Minimization(AM) methods have emerged as potential solutions for deep learning problems. These methods reformulate a neural network problem as a nested function with multiple linear and nonlinear transformations across layers. The nested structure is decomposed into a series of linear and nonlinear equality constraints using auxiliary variables and penalty hyperparameters. This decomposition generates subproblems that can be minimized alternately.

Several recent methods, including the Alternating Direction Method of Multipliers (ADMM), Block Coordinate Descent (BCD), and Method of Auxiliary Coordinates (MAC), have been applied to replace the nested neural network with a constrained problem without nesting. These methods exhibit good scalability in terms of the number of layers and high accuracy on test sets. They also overcome gradient vanishing issues, allow for non-differentiable activation functions, and accommodate complex non-smooth regularization and constraints, which are important for practical requirements such as interpretability, energy-efficiency, and cost awareness.

Let's formulate the following Multiple-Layer Perceptron(MLP) Learning problem as follows: A typical MLP model consists of $ L $ layers, each of which are defined by a linear mapping and a nonlinear activation function. A linear mapping is composed of  a weight vector $ W_l\in \mathbb{R}^{n_l\times n_{l-1}}$ , where $n_l$ is the number of neurons on the $l$-th layer; a nonlinear mapping is defined by a  continuous activation function $h_l(\bullet)$. Given an input $a_{l-1}\in \mathbb{R}^{n_{l-1}}$ from the $(l-1)$-th layer, the $l$-th layer outputs $a_l=h_l(W_la_{l-1})$. By introducing an auxiliary variable $z_l$ as the output of the linear mapping, the neural network problem is formulated mathematically as follows:

$$\begin{equation}\min_{a_l,W_l,z_l} R(z_L;y). \ s.t.\ z_l=W_la_{l-1}\ (l=1,\cdots,L), \ a_l=h_l(z_l) \ (l=1,\cdots,L-1)\end{equation}$$

<p style="text-align: center;"><strong>ADMM for Efficient Deep Learning with Global Convergence</strong></p>

<p align="center">
<img src="https://raw.githubusercontent.com/xianggebenben/Junxiang_Wang.github.io/master/images/dlADMM.jpg" alt="drawing" width="1000"/>
</p>

**Junxiang Wang**, Fuxun Yu, Xiang Chen, and Liang Zhao. ADMM for Efficient Deep Learning with Global Convergence. in Proceedings of the 25th ACM SIGKDD Conference on Knowledge Discovery and Data Mining (KDD 2019), research track (acceptance rate: 14.2%), Alaska, USA, Aug 2019. [paper](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/KDD2019/dlADMM_main.pdf) [material](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/KDD2019/dlADMM_supplementary.pdf) [code](https://github.com/xianggebenben/dlADMM) [video](https://www.youtube.com/watch?v=J3pCqVhud_M) [slides](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/KDD2019/ADMM%20for%20Efficient%20Deep%20Learning%20with%20Global%20Convergence.pdf) [poster](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/KDD2019/poster.pdf) [Chinese media coverage](https://www.jiqizhixin.com/articles/2019-08-29-9)

In this paper, we relax Equation(1) to the following:
$$ \min_{W_l,z_l,a_l}R(z_L;y)+(\nu/2)\sum_{l=1}^{L-1}(\Vert z_l-W_la_{l-1}\Vert^2_2+\Vert a_l-f_l(z_l)\Vert^2_2)$$
$$s.t. \ z_L=W_La_{L-1}$$

where $\nu>0$ is a tunning parameter. We propose a novel optimization framework for deep learning via ADMM (dlADMM). The parameters in each layer are updated backward and then forward so that the parameter information in each layer is exchanged efficiently. The time complexity is reduced from cubic to quadratic in (latent) feature dimensions via a dedicated algorithm design for subproblems that enhances them utilizing iterative quadratic approximations and backtracking. Finally, we provide the first proof of global convergence for an ADMM-based method (dlADMM) in a deep neural network problem under mild conditions.

<p style="text-align: center;"><strong>Accelerated Gradient-free Neural Network Training by Multi-convex Alternating Optimization</strong></p>

**Junxiang Wang**, Hongyi Li, and Liang Zhao. Accelerated Gradient-free Neural Network Training by Multi-convex Alternating Optimization. Neurocomputing, (impact factor: 5.719), 2022. [paper](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/Neurocomputing2022/mDLAM.pdf) [code](https://github.com/xianggebenben/mDLAM)

In this paper, we tackle Equation(1) by introducing inequality constraints as follows:

$$\min{W_l,z_l,a_l} R(z_L;y)+(\rho/2)\sum\nolimits_{l=1}^L\Vert z_l-W_la_{l-1}\Vert^2_2 \ s.t. \ h_l(z_l)-\varepsilon\leq a_l\leq h_l(z_l)+\varepsilon$$

where $\rho>0$ and $\varepsilon>0$ is tuning parameters. We propose a novel monotonous Deep Learning Alternating Minimization (mDLAM) algorithm. Our innovative inequality-constrained formulation infinitely approximates the original problem with non-convex equality constraints, enabling our convergence proof of the proposed mDLAM algorithm regardless of the choice of hyperparameters. Our mDLAM algorithm is shown to achieve a fast linear convergence by the Nesterov acceleration technique.

<p style="text-align: center;"><strong>Toward Model Parallelism for Deep Neural Network based on Gradient-free ADMM Framework</strong></p>

<p align="center">
<img src="https://raw.githubusercontent.com/xianggebenben/Junxiang_Wang.github.io/master/images/pdadmm.png" alt="drawing" width="1000"/>
</p>

**Junxiang Wang**, Zheng Chai, Yue Cheng, Liang Zhao. Toward Model Parallelism for Deep Neural Network based on Gradient-free ADMM Framework. in Proceedings of the IEEE International Conference on Data Mining (ICDM 2020), regular paper (acceptance rate: 9.8%), Sorrento, Italy, Nov 2020. [paper](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/ICDM2020/pdADMM.pdf) [code](https://github.com/xianggebenben/pdADMM) [slides](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/ICDM2020/pdADMM%20presentation.pdf)

In this paper, we address Equation(1) by breaking layer dependency in order to achieve model parallelism. Specifically, we introduce two variables $p_l$ and $q_l$ by relaxing Equation(1) to the following:
$$\min_{p_l,W_l,z_l,q_l} R(z_L;y)+(\nu/2)(\sum_{l=1}^{L}\Vert z_l-W_lp_l\Vert^2_2+\sum\nolimits_{l=1}^{L-1}\Vert q_l-f_l(z_l)\Vert^2_2)\ s.t. \ p_{l+1}=q_l$$

where $p_l$ and $q_l$ are the input and the output of the $l$-th layer, respectively, and $\nu>0$ is a tuning parameter. We propose a novel parallel deep learning ADMM framework (pdADMM) to achieve layer parallelism: parameters in each layer of neural networks can be updated independently in parallel. The convergence of the proposed pdADMM to a critical point is theoretically proven under mild conditions. The convergence rate of the pdADMM is proven to be $o(1/k)$ where $k$ is the number of iterations.

<p style="text-align: center;"><strong>Towards Quantized Model Parallelism for Graph-Augmented MLPs Based on Gradient-Free ADMM Framework</strong></p>
<p align="center">
<img src="https://raw.githubusercontent.com/xianggebenben/Junxiang_Wang.github.io/master/images/gamlp_framework.png" alt="drawing" width="1000"/>
</p>

**Junxiang Wang**, Hongyi Li(first-coauthor), Zheng Chai, Yongchao Wang, Yue Cheng, and Liang Zhao. Towards Quantized Model Parallelism for Graph-Augmented MLPs Based on Gradient-Free ADMM Framework. IEEE Transactions on Neural Networks and Learning Systems, (impact factor: 14.255)，2022. [paper](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/TNNLS2022/GA_MLP.pdf) [code](https://github.com/xianggebenben/pdADMM-G)

In this paper, we apply the pdADMM algorithm to the GA-MLP models for graph learning, which first augment the node features and then imposing node-wise functions based on Multi-Layer Perceptron(MLP). We propose a  parallel graph deep learning Alternating Direction Method of Multipliers (pdADMM-G) framework to achieve model parallelism: parameters in each layer of GA-MLP models can be updated in parallel. The extended pdADMM-G-Q algorithm reduces communication costs by introducing the quantization technique. Theoretical convergence to a (quantized) stationary point of the pdADMM-G algorithm and the pdADMM-G-Q algorithm is provided with a sublinear convergence rate $o(1/k)$, where $k$ is the number of iterations.
