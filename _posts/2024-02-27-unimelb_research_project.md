---
layout: post
title: "Unimelb Research Project"
date:   2024-02-27
tags: [research, Computer Vision, Image Segmentation]
comments: true
author: allen
---

The rise of deep neural networks has resulted in a great improvement in the performance of medical image segmentation. This project aims to explore the development of automated analysis of renal tumors as depicted in abdominal computed tomography (CT) images. Starting with semantic segmentation of the kidney, we aim to identify renal tumors and kidney sub-structures (e.g. cortex, medulla) in order to facilitate automated reasoning regarding diagnosis and therapy decision.

**Research Topic Title:** Automated Analysis of Depiction of Renal Cancers in Abdominal CT Images (Brian Chapman)

**Supervisor:** Brian Chapman

# Research Proposal

<embed src="/images/2024-02-01-unimelb_research_project/Research Proposal_v2.pdf" width="100%" height="700px" type="application/pdf">

# Thesis

<embed src="/images/2024-02-01-unimelb_research_project/COMP90055_Thesis_finalv2.pdf" width="100%" height="700px" type="application/pdf">


# Part of Inspirations during researching
The following inspirations are from literature review.

1. The original is better.
    - We believe that removing the redundant frills in many network designs and focusing on other aspects can improve the performance and universality of the method [1].
    - A large number of experiments have shown that the original U - Net network is usually more robust than its variants [4].
    - The plain “nnU - Net” demonstrated the best performance, despite several teams' efforts to enhance it [6]. 

2. Optimization in non - model aspects is of great importance.
    - The remaining interdependent choices regarding the precise architecture, pre - processing, training, inference, and post - processing often lead to poor performance of U - Net when used as a benchmark. Additionally, if the network has not been fully optimized for the task at hand, it is easy to demonstrate that architectural adjustments aimed at improving network performance are effective, thus leaving sufficient room for adjustments to improve the results. However, in our own preliminary experiments, these adjustments failed to improve the segmentation results in a fully optimized network, and thus are unlikely to advance the state - of - the - art. This makes us believe that the influence of non - model aspects in the segmentation method is greater, yet severely underestimated [1].
    - When ranking among the top 15 in the KiTS19 challenge, the absence of any commonly used architectural modifications (such as residual connections [26, 10], dense connections [18, 15], attention mechanisms [30], or dilated convolutions [5, 24]) represents a necessary condition for good performance on the KiTS task [2].
    - The performance improvement of the architectural extensions proposed in the literature may not extend beyond the datasets for which they were proposed, as the quality of hyperparameter configuration often obscures the effects of the evaluated architectural modifications [2]. 
    * Litjens et al. concluded that "the exact architecture is not the most important determinant in getting a good solution" 【3】
    * The winning approach of Isensee et al. focuses primarily on data preprocessing rather than novel architectures or optimization algorithms. [6]

3. The receptive field of nnU - net is limited [1]. – Improvement point: Increase the receptive field.
The 3D U - net in nnU - net is restricted by the amount of available GPU memory, which only allows us to train this architecture on image patches [1]. – Improvement point: Train this framework with full - scale images.

4. To address the foreground/background imbalance problem, cascaded segmentation can be considered [5]. 

## References:

1. Isensee, F., Petersen, J., Klein, A., Zimmerer, D., Jaeger, P. F., Kohl, S., ... & Maier-Hein, K. H. (2018). nnu-net: Self-adapting framework for u-net-based medical image segmentation. arXiv preprint arXiv:1809.10486.
2. Isensee, F., Jaeger, P. F., Kohl, S. A., Petersen, J., & Maier-Hein, K. H. (2021). nnU-Net: a self-configuring method for deep learning-based biomedical image segmentation. Nature methods, 18(2), 203-211.
3. Litjens, G., Kooi, T., Bejnordi, B. E., Setio, A. A. A., Ciompi, F., Ghafoorian, M., ... & Sánchez, C. I. (2017). A survey on deep learning in medical image analysis. Medical image analysis, 42, 60-88.
4. Liu, J., Yildirim, O., Akin, O., & Tian, Y. (2023). AI-driven robust kidney and renal mass segmentation and classification on 3D CT images. Bioengineering, 10(1), 116.
5. Abdelrahman, A., & Viriri, S. (2023). Efficientnet family u-net models for deep learning semantic segmentation of kidney tumors on ct images. Frontiers in Computer Science, 5, 1235622.
6. Heller, N., Isensee, F., Maier-Hein, K. H., Hou, X., Xie, C., Li, F., ... & Weight, C. (2021). The state of the art in kidney and kidney tumor segmentation in contrast-enhanced CT imaging: Results of the KiTS19 challenge. Medical image analysis, 67, 101821.


# Future Improvements
1. Try other datasets, experiment with different tuning parameters, expand the functionality, generalization ability, and universality of the network, and enhance its robustness.
2. Tuning: Pre - processing (such as resampling and standardization), training (such as loss, optimizer settings, and data augmentation), inference (such as patch - based strategies and model ensembling by extending across test time), and potentially post - processing (such as performing single connected component analysis, if applicable).
3. Increase efforts in non - architectural aspects. In the segmentation method, non - architectural factors (such as data processing and training strategies) may have a greater impact than the architecture itself, but they are often severely underestimated.
4. Conduct more ablation experiments. 