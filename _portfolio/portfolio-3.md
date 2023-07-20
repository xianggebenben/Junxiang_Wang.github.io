---
title: "Graph Inverse Problems"
excerpt:
collection: portfolio
---

Graphs are universal structures consisting of nodes and links. They have a wide range of applications in various domains such as social networks, biology, and recommender systems. Graph prediction problems involve predicting outcomes of nodes, links, or entire graphs. While these problems have been extensively studied, graph inverse problems, which involve backtracking graph inputs to achieve specific graph outputs, are less explored and represent open research areas. Graph inverse problems have significant applications, including graph source localization and network influence maximization. For instance, graph source localization identifies information sources in a graph that result in current information diffusion patterns, and it can be viewed as the reverse process of graph diffusion.

<p style="text-align: center;"><strong>An Invertible Graph Diffusion Neural Network for Source Localization</strong></p>

<p align="center">
<img src="https://raw.githubusercontent.com/xianggebenben/Junxiang_Wang.github.io/master/images/IVGD.png" alt="drawing" width="1000"/>
</p>

**Junxiang Wang**, Junji Jiang, and Liang Zhao. An Invertible Graph Diffusion Neural Network for Source Localization. 31th International World Wide Web Conference (WWW 2022), (acceptance rate: 17.7%), Lyon, FR, Apr 2022. [paper](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/WWW2022/IVGD.pdf) [code](https://github.com/xianggebenben/IVGD) [slides](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/WWW2022/IVGD_slides.pdf)

In this paper, we establish a generic framework of invertible graph diffusion models for source localization on graphs, namely Invertible Validity-aware Graph Diffusion (IVGD). Specifically, first, to inversely infer sources of graph diffusion, we propose a graph residual scenario to make existing graph diffusion models invertible with theoretical guarantees; second, we develop a novel error compensation mechanism that learns to offset the errors of the inferred sources. Finally, to ensure the validity of the inferred sources, a new set of validity-aware layers have been devised to project inferred sources to feasible regions by flexibly encoding constraints with unrolled optimization techniques. A linearization technique is proposed to strengthen the efficiency of our proposed layers. The convergence of the proposed IVGD is proven theoretically.

<p style="text-align: center;"><strong>Source Localization of Graph Diffusion via Variational Autoencoders for Graph Inverse Problems</strong></p>
Chen Ling, Junji Jiang, **Junxiang Wang** and Liang Zhao. Source Localization of Graph Diffusion via Variational Autoencoders for Graph Inverse Problems. in Proceedings of the 28th ACM SIGKDD Conference on Knowledge Discovery and Data Mining (KDD 2022), research track (acceptance rate: 15.0%), Washington D.C, USA, Aug 2022. [paper](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/KDD2022/SLVAE.pdf) [code](https://github.com/triplej0079/SLVAE)

In this paper, we present a generic framework: Source Localization Variational AutoEncoder (SL-VAE) for locating the diffusion sources under arbitrary diffusion patterns. Particularly, we propose a probabilistic model that leverages the forward diffusion estimation model along with deep generative models to approximate the diffusion source distribution for quantifying the uncertainty. SL-VAE further utilizes prior knowledge of the source-observation pairs to characterize the complex patterns of diffusion sources by a learned generative prior. Lastly, a unified objective that integrates the forward diffusion estimation model is derived to enforce the model to generalize under arbitrary diffusion patterns.

<p style="text-align: center;"><strong>Deep Graph Representation Learning and Optimization for Influence Maximization</strong></p>
<p align="center">
<img src="https://raw.githubusercontent.com/xianggebenben/Junxiang_Wang.github.io/master/images/DeepIM.png" alt="drawing" width="1000"/>
</p>
Chen Ling, Junji Jiang, **Junxiang Wang**, My Thai, Lukas Xue, James Song, Meikang Qiu, and Liang Zhao. Deep Graph Representation Learning and Optimization for Influence Maximization. In proceedings of the International Conference on Machine Learning (ICML 2023), (acceptance rate: 27.9%), Honolulu, Hawaii, USA, July 2023. [paper](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/ICML2023/paper.pdf) [code](https://github.com/triplej0079/DeepIM)

In this paper, we design a novel framework DeepIM to generatively characterize the latent representation of seed sets for the influence maximization problem, and we propose to learn the diversified information diffusion pattern in a data-driven and end-to-end manner. Finally, we design a novel objective function to infer optimal seed sets under flexible node-centrality-based budget constraints.

**Dataset**
We provide the following benchmark networks for download:
| Network            | #Node | #Edge | Average  Degree | Diameter | Download Link |
|------------------|-------|-------|-----------------|----------|------|
| Karate           | 34    | 78    | 2.294           | 5        |      |
| Dolphins         | 62    | 159   | 5.129           | 8        |      |
| Jazz             | 198   | 2742  | 13.848          | 9        |      |
| Network  Science | 1589  | 2742  | 3.451           | 17       |      |
| Cora-ML          | 2810  | 7981  | 5.680           | 17       |      |
| Power  Grid      | 4941  | 6594  | 2.669           | 46       |      |

[This script]() provides the simulation of information diffusion using the above networks by five diffusion models: (IM), (LT), (SI), (SIR) and (SIS). Please cite our paper if you use our datasets in your paper:

@inproceedings{wang2022invertible,
  title={An invertible graph diffusion neural network for source localization},
  author={Wang, Junxiang and Jiang, Junji and Zhao, Liang},
  booktitle={Proceedings of the ACM Web Conference 2022},
  pages={1058--1069},
  year={2022}
}
