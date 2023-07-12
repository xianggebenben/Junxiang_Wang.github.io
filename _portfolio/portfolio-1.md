---
title: "Vaccine Adverse Event Detection on Social Media"
excerpt:
collection: portfolio
---

A wide range of vaccinations have made a significant positive impact on global health. However, vaccinations can sometimes cause adverse reactions in a large population, which has become a significant healthcare issue. Severe reactions can even lead to death. To address the importance and potential consequences of adverse reactions, there is a need for a system that can quickly and accurately identify such events. The FDA's Sentinel Initiative is an example of such a system. However, the traditional method of gathering Adverse Event(AE) reports relies on users submitting detailed descriptions through complex forms after recovering from the reactions. This system has two major drawbacks: a low number of formal reports due to complexity, and a time delay in submitting reports due to administrative processes. In contrast, social media platforms like Twitter and Facebook have become popular channels for sharing information, including healthcare-related updates.

<p style="text-align: center;"><strong>Semi-supervised Multi-instance Interpretable Models for Flu Shot Adverse Event Detection</strong></p>

**Junxiang Wang**, Liang Zhao, and Yanfang Ye. Semi-supervised Multi-instance Interpretable Models for Flu Shot Adverse Event Detection. 2018 IEEE International Conference on Big Data (BigData 2018) (acceptance rate: 18.9%), Seattle, USA, Dec 2018. [paper](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/BigData2018/nSSM.pdf) [code](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/BigData2018/BigData2018.zip) [slides](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/BigData2018/Semi-supervised%20Multi-instance%20Interpretable%20Models%20for%20Flu%20Shot%20Adverse%20Event%20Detection.pdf)

In this paper, we present a new semi-supervised multi-instance learning model to detect potential adverse events reflected by social media, which will facilitate the further clinical verification and prompt intervention. Specifically, given only  user-level labels, this model interpretably identifies the user's adverse-event-indicative messages by employing a multi-instance learning strategy; unlabeled users' messages are also utilized to improve classifier performance by a semi-supervised term. Two  models and corresponding   algorithms, namely the non-smooth Semi-Supervised Multi-instance (nSSM) algorithm and the smooth Semi-Supervised Multi-instance (sSSM) algorithm, have been developed to optimize parameters accurately and efficiently.


<p style="text-align: center;"><strong>Adverse Event Detection by Integrating Twitter Data and VAERS</strong></p>

<img src="https://raw.githubusercontent.com/xianggebenben/Junxiang_Wang.github.io/master/images/MILR.jpg" alt="drawing" width="1000"/>


**Junxiang Wang**, Liang Zhao, Yanfang Ye, and Yuji Zhang. Adverse event detection by integrating Twitter data and VAERS. Journal of Biomedical Semantics, (impact factor: 1.845), 2018. [paper](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/JBMS2018/paper.pdf)

In this paper, we develop a combinatorial classification approach by integrating Twitter data and the Vaccine Adverse Event Reporting System (VAERS) information aiming to identify potential adverse events after influenza vaccine. Specifically, we combine formal reports which have accurately predefined labels with social media data to reduce the cost of manual labeling; in order to combat the class imbalance problem, a max-rule based multi-instance learning method is proposed to bias positive users. Various experiments were conducted to validate our model compared with other baselines. We observed that (1) multi-instance learning methods outperformed baselines when only Twitter data were used; (2) formal reports helped improve the performance metrics of our multi-instance learning methods consistently while affecting the performance of other baselines negatively; (3) the effect of formal reports was more obvious when the training size was smaller. Case studies show that our model labeled users and tweets accurately.

<p style="text-align: center;"><strong>Multi-instance Domain Adaptation for Vaccine Adverse Event Detection</strong></p>

<img src="https://raw.githubusercontent.com/xianggebenben/Junxiang_Wang.github.io/master/images/MIDA.png" alt="drawing" width="800"/>

**Junxiang Wang** and Liang Zhao. Multi-instance Domain Adaptation for Vaccine Adverse Event Detection. 27th International World Wide Web Conference (WWW 2018), (acceptance rate: 14.8%), Lyon, FR, Apr 2018. [paper](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/WWW2018/MIDA.pdf) [code](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/WWW2018/MIDA.zip) [slides](https://github.com/xianggebenben/Junxiang_Wang.github.io/blob/master/supplementary_material/WWW2018/Multi-instance%20Domain%20Adaptation%20for%20Vaccine%20Adverse%20Event%20Detection_modified.pdf)

In this paper, we propose a novel generic framework named Multi-instance Domain Adaptation (MIDA) to maximize the synergy between  traditionally formal reporting systems and social media in the vaccine adverse event detection task for social media users. Specifically, we propose a generalized Maximum Mean Discrepancy (MMD) criterion to measure the semantic distances between the heterogeneous messages from these two domains in their shared latent semantic space. Then these message-level generalized MMD distances are synthesized by newly proposed mixed instance kernels to user-level distances. We finally minimize the distances between the samples of the partially-matched classes from these two domains. In order to solve the non-convex optimization problem, an efficient Alternating Direction Method of Multipliers (ADMM) based algorithm combined with the Convex-Concave Procedure (CCP) is developed to optimize parameters accurately.
