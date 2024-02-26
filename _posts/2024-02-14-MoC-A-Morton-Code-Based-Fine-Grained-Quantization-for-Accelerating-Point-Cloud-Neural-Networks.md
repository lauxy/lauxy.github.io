---
# layout: post
# title: [Paper] MoC: A Morton-Code-Based Fine-Grained Quantization for Accelerating Point Cloud Neural Networks
# subtitle: Excerpt from Soulshaping by Jeff Brown
# cover-img: /assets/img/post/moc-algorithm.png
thumbnail-img: /assets/img/post/moc-algorithm.png
# share-img: /assets/img/post/moc-algorithm.png
# tags: [Point Cloud Neural Network, AI accelerator]
# author: Xueyuan Liu, Zhuoran Song, Hao Chen, Xing Li, and Xiaoyao Liang
---

Point Cloud Neural Network (PCNN) plays an essential role in various 3D applications, with some of them even being time-sensitive and safety-critical. However, the large scale of unordered points with lengthy features results in heavy computational workloads, making them far from real-time processing. To address this challenge, we propose MoC, a Morton-code-based fine-grained quantization for accelerating PCNNs. Specifically, we utilize Morton code to capture the spatial locality among points. Then, we gather nearby points with similar features into a region. Considering the similarity in features of nearby points, we propose to decompose features into base and offsets, where the offsets fall within a narrow range. Building upon this, we introduce a two-level mixed-precision quantization. In the first level, we quantize offsets with low precision, while keeping the base in high precision to ensure accuracy. For the second level, noticing the different data distribution of offsets across various regions, we employ two types of low precision at the region level, which provides opportunities to further accelerate feature computations. To support our algorithm, we design a hardware architecture that parallelizes the Morton code path with the critical path. In our extensive experiments on various datasets, our algorithm-architecture co-designed method demonstrates 12x, 6.3x, 4.7x, 3.8x, 3.4x and 2.8x speedup and 19.3x, 9.7x, 6.0x, 5.2x, 4.6x and 4.1x energy savings over CPU, Server and Edge GPUs, state-of-the-art ASICs (\textit{incl.} PointAcc, MARS, PRADA) with negligible accuracy loss.


Authors: **Xueyuan Liu**, Zhuoran Song, Hao Chen, Xing Li, and Xiaoyao Liang


![moc](/assets/img/post/moc-algorithm.png)

* Accepted by Design Automation Conference (DAC 2024, CCF-A).
* [paper]() (coming soon...)
* [cite]() (coming soon...)