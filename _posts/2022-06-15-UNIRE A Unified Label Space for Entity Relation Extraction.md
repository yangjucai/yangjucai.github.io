---
layout: post
title: UNIRE
categories: [paper translation, entity relation extration]
description: UNIRE A Unified Label Space for Entity Relation Extraction
keywords: entity relation extraction
---

  <h2 align="center">UNIRE：一个统一label空间的实体关系抽取</h2>



<center>Department of Computer Science and Engineering, Shanghai Jiao Tong University</center>
<center>MoE Key Lab of Artificial Intelligence, AI Institute, Shanghai Jiao Tong University</center>
<center>School of Computer Science and Technology, East China Normal University</center>
<center>ByteDance AI Lab</center>
<center>{yjwang.cs, yanjunchi}@sjtu.edu.cn ybwu@cs.ecnu.edu.cn</center>
<center>{sunchangzhi, zhouhao.nlp, lileilab}@bytedance.com</center>
<p align="right">
    ------------------JC 译
</p>

**摘要：**许多联合的实体关系抽取模型为两个子任务建立两个独立的label空间（例如，实体识别和关系分类）。我们认为这种设置会隐藏实体和关系之间的关联信息。在这项工作中，我们消除了对这两个子任务的label空间处理方法的不同。我们模型的输入是一个包含一个句子中说有单词对的表。在这给表中，实体和关系用正方形和长方形表示。我们应用了统一的分类器来预测每个格子的label，这统一了两个子任务的学习。为了测试，一个高效的（并且快速的）近似编码器被提出用来在表中找出正方形和长方形。在三个基准（ACE04，ACE05，ACE06）上的实验表明，仅仅使用一般数量的参数，我们的模型拥有最好的抽取器，取得了有竞争力的准确性，并且它是更快的。



## 1	介绍

从纯文本中提取结构化信息是自然语言处理中的长期研究课题。典型的，它的目的是识别特定的实体和关系来分析句子的语义。一个例子如图一所示，一个人物实体”David Perkins“和一个地理实体”California“有一个物理位置关系PHYS。

![image-20220623091020720](https://cdn.jsdelivr.net/gh/yangjucai/yangjucai.github.io@main/images/postsimage-20220623091020720.png)

识别实体和关系的方法可以被归类为流水线模型和联合模型。在流水线模型的设置中，实体模型和关系模型是独立并拥有分离的特征空间和输出label空间。另一方面，在联合模型的设置中，一些共享特征空间或者交互解码的参数被用于探讨两种任务的共同结构。人们普遍认为联合模型可能更好因为他们能够在子模型中减少错误的传播，有更少参数集和在两种任务上的统一编码先验知识（例如，约束）。

然而，Zhong和Chen最近表示在现代预训练工具的帮助下（例如，BERT），将实体和关系模型分离（有独立的编码器和流水线解码）能够超过现存的联合模型。他们认为，既然实体和关系模型输出的label空间是不同的，相比于共享的编码器，分离的编码器能够更好的捕获确切的上下文信息，避免他们中潜在的的冲突，并且帮助解码器做出更准确地预测，即分离的label空间需要分离的编码器。

在这篇文章中，我们追求一个用于实体关系抽取的更好的联合模型。重新研究现存的方法后，我们发现尽管实体模型和关系模型共享编码器，通常情况下他们的label空间仍然是分离的（尽管在有联合解码器的模型中）。因此，与（Zhong and Chen, 2020）相似，我们会有疑问，是否联合编码器（解码器）需要联合的label空间。

实现统一实体关系label空间的难点在于两个子任务通常被定为两种不同的学习问题（例如，实体检测被认为是序列label问题，关系分类被认为是多类分类问题），并且他们的label被放到不同的事情上（例如单词 v.s. 单词对）。一种先前的尝试是用一种序列label模型来处理这两个子任务。复合的label集被设计用来对实体和关系编码。然而，这丢失了模型的表现力：它既不能检测重叠的关系（例如，参加多个关系的实体），也不能检测孤立的关系（例如，没有出现在任何关系中的实体）。

我们定义一个统一label空间的关键想法是，如果我们认为Zheng 等人的解决方法是在实体label的过程中执行关系分类，我们也将把实体检测看作关系分类的一个特例来考虑反向的问题。我们新的输入空间是一个每个输入都对应句子中的一个单词对的二维表（图一）。这种联合模型从一个统一的label空间中将label分配给每一个单元格。（实体类型集合和关系类型集合的并集）。在图形上，实体是对角线上的正方形，关系是对角线外的长方形。这种方式保留的现存实体关系抽取场景的全部模型表达(例如，重叠关系、有向关系、无向关系)。他也不同于现在用于实体关系抽取的,对实体和关系仍然有分离的label空间，并且分别处理对角线上和对角线外地输入地表格填充设置.

基于这个表格公式，我们的联合实体关系抽取实现两个动作，填充和解码。首先，填充表格是用来预测每个单词对的label，这与依赖解析中的弧度预测类似。我们采用了双仿射注意力机制来学习单词对的交互关系。我们也在结构规格化的过程中加入了两个结构化约束。其次，给定了填有label对数的表格，我们设计了一个仅是联合解码算法来输出最终抽取的实体和关系。基本上，它能够有效地发现表格上分离的点来识别正方形和长方形（这也不同于现存的，仍然使用特定序列解码并且递增的填充表格的表格填充模型）。

基于三种基准（ACE04，ACE05，SciERC）的实验结果表明，提出的联合方法相比于最高水平的抽取器获得了有竞争力的表现：我们的方法在ACE04和SciERC上更好，并且在ACE05上相当有竞争力。同时，我们新的联合模型在解码上是相当快的（比精确的流水线实现快10倍，能够媲美比性能更低的近似流水线的速度）。它也具有更小的参数集：相比于分离的编码器，共享的编码器仅仅使用半数的参数。

## 2	任务定义

