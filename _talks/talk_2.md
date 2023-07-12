---
title: "Towards Quantized Model Parallelism for Graph-Augmented MLPs Based on Gradient-Free ADMM Framework"
collection: talks
type: "Talk"
permalink: /talks/talk_2
venue: "INFORMS Optimization Society Conference (IOS)"
date: 2022-03-15
location: "Greenville, SC, United States"
---
[slides](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/IOS2022/IOS_2022_talk.pdf)

Abstract: While Graph Neural Networks (GNNs) are popular in the deep learning community, it suffers from several challenges including over-smoothing, exploding, or vanishing gradients in training. Recently, a series of models have attempted at relieving these issues by first augmenting the node features and then imposing node-wise functions based on Multi-Layer Perceptron (MLP), which are widely referred to as GA-MLP models. However, while GA-MLP models enjoy deeper architectures for better accuracy, their efficiency largely deteriorates. Moreover, popular acceleration techniques such as stochastic-version or data-parallelism cannot be effectively applied due to the dependency among samples (i.e., nodes) in graphs. To address these issues, in this paper, instead of data parallelism, we propose a parallel graph deep learning Alternating Direction Method of Multipliers (pdADMM-G) framework to achieve model parallelism: parameters in each layer of GA-MLP models can be updated in parallel. The extended pdADMM-G-Q algorithm reduces communication costs by utilizing the quantization technique. Theoretical convergence to a stationary point is provided with a sublinear convergence rate o(1/k). Extensive experiments in six benchmark datasets demonstrate that the proposed algorithms lead to high speedup, and outperform all the existing state-of-the-art comparison methods. Moreover, the pdADMM-G-Q algorithm reduces communication overheads by 25% without loss of performance.
