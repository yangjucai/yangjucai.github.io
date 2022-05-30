---
layout: post
title: 手语生成的渐进式转换器
categories: [paper translation, sign language production]
description: Progressive Transformers for End-to-End Sign Language Production
keywords: sign language production
---

<h2 align="center">手语生成的渐进式转换器</h2>
<h5 align="center">
    Ben Saunders, Necati Cihan Camgoz, and Richard Bowden
</h5>
<h5 align="center">
    University of Surrey
</h5>
<h5 align = "center">
    {b.saunders,n.camgoz,r.bowden}@surrey.ac.uk
</h5>
<p align="right">
    ------------------JC 译
</p>

**摘要**  自动手语生成（SLP）的目的是将口语转换成在一定程度上能够媲美人工翻译的连续手语视频流。如果这是可行的，这将彻底改变聋人的交流方式。之前主要对孤立手语生成的研究工作表明更适合于全符号连续域的架构的必要性。
在这篇论文中，我们提出了渐进式转换器，这是第一个以端到端的方式将分离的口语语句翻译为连续3D手语姿态序列的手语生成模型。我们引入了一个新奇的计数器解码技术，这实现了训练和推理时的连续序列生成。我们展示了两种模型的配置方案，一个直接从文本生成手语的端到端的网络，和一个利用光泽的栈式网络。我们也提供了多个数据扩充过程来克服数据倾斜问题并且极大程度上提高了手语生成模型的性能。
我们为手语生成提出一种反向评估机制，在挑战RWTH-PHOENIX-Weather-2014T(PHOENIX14T)数据集和为后续研究指定基准时展示基准量化结果。代码可以在<a href="https://github.com/BenSaunders27/ProgressiveTransformersSLP">https://github.com/BenSaunders27/ProgressiveTransformersSLP 获得。</a>

