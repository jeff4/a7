---
layout: ../../layouts/MarkdownPostLayout.astro
title: 'Goodfellow (GBC) Chap 8'
pubDate: 2023-11-15
LastUpdatedDate: 2023-12-28
CreatedDate: 2023-10-28
description: 'Selected notes from Chapter 8 (Optimization)'
author: 'Jeff'
tags: []
---

**Deep Learning (2016)** 
* Ian Goodfellow, Yoshua Bengio, and Aaron Courville
* GBC

## Chapter 8: Optimization for Training Deep Models p. 267
1. Deep learning algorithims involve optimization in many contexts.
1. For example, performing inference in models such as PCA involves solving an optimization problem. 
1. We often use analytical optimization to write proofs or design algorithms.
1. Of all the many optimization problems involved in deep learning, ANN training is the most difficult.
	* It is quite common to invest days to months of time on hundreds of machines to solve even a single instance of the neural network training problem. 
	* Because this problem is so important and so expensive, a specialized set of optimization techniques have been developed for solving it. 
1. Chapter 8 presents the best optimization techniques for training ANNs.

### JH Break

1. 






### Notes from December 2023
1. GBC Chapter 8, section 8.3 is on Stochastic Gradient Descent (SGD)
1. AdaGrad and then in section 8.5.3 Adam adaptive learning rate optimization * Batch Normalization is extremely exciting circa 2015 (section 8.7.1) * section 8.7.4 Supervised Pretraining

##### Double-struck R for Real numbers
* "rp = double-struck R = &#8477;
* "tp = theta = **&#952;**
* "hp = theta-hat = **&#952;-hat**
* "pp = vector arrow above prior character = &#8407;
* "yp = lowercase phi = &#966;
* "ip = infinity = &#8734;
* "ap = rightward pointing arrow = &#8594;
* "ep = element of = &#8712;
* "wp = matrix W = **`W`**
* "sp = lowercase sigma for sigmoid function &#963;
* "np = nabla aka gradient upside down triangle &#8711;
* "op = omega = &#937;
* "jp = Capital letter J function with a tilde above it = J&#771;

