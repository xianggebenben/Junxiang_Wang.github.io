---
title: "Power of Alternating Direction Method of Multipliers(ADMM) in deep learning"
collection: talks
type: "Talks"
permalink: /talks/talk_3
venue: "Modeling and Optimization, Theory and Applications (MOPTA)"
date: 2021-08-02
location: "Bethlehem, PA, United States"
---

[slides](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/MOPTA2021/MOPTA_talk.pdf)

Abstract: The Alternating Direction Method of Multipliers(ADMM) has been demonstrated powerful performance in many conventional machine learning applications and is recently considered to be a potential alternative to Stochastic Gradient Descent(SGD) as a deep learning optimizer. However, several challenges remain in this emerging domain, including slow convergence towards solutions, the expensive computational cost, and the lack of theoretical convergence guarantees. In this talk, I introduce a novel optimization framework for deep learning via ADMM(dlADMM) to address them simultaneously. Specifically, the parameters in each layer are updated backward and then forward so that the parameter information in each layer is exchanged efficiently; the computational cost is reduced from cubic to quadratic via a dedicated algorithm design for subproblems that enhances them utilizing iterative quadratic approximations and backtracking. Moreover, we provide proof of convergence to a critical point for an ADMM-based method(dlADMM) in a neural network problem under mild conditions. In order to achieve model parallelism, we extend our dlADMM framework to parallel deep learning ADMM framework(pdADMM): parameters in each layer of neural networks can be updated independently in parallel. Extensive experiments on multiple benchmark datasets demonstrate that our proposed dlADMM and pdADMM outperform most of the comparison methods, and the pdADMM can lead to more than 10 times speedup for training large-scale deep neural networks.
