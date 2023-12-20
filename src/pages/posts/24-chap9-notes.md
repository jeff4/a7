---
layout: ../../layouts/MarkdownPostLayout.astro
title: 'Goodfellow (GBC) Chap 9'
pubDate: 2023-11-15
LastUpdatedDate: 2023-12-28
CreatedDate: 2023-10-28
description: 'Notes from Chapter 9 Convolutional Networks'
author: 'Jeff'
tags: []
---

**Deep Learning (2016)** 
* Ian Goodfellow, Yoshua Bengio, and Aaron Courville
* GBC
## Chapter 9: Historical notes from end of CNNs
### 9.11 CNNs and the History of Deep Learning
* CNNs are a key example of a successful application of insights obtained by studying the brain. p. 359
* They were also some of the first deep models to perform well, long before arbitrary deep models were considered viable.
* CNNs were also some of the first neural networks to solve important commercial applications and remain at teh forefront of such applications all the way to day (as of 2016).
* For example, in the 1990s, the neural network research group at AT&T developed a convultional network for reading checks. See Yann LeCun, Bottou, Yoshua Bengio, and Haffner (1998) "Gradient-based learning applied to document recognition." *Proc. IEEE*
	* By the end of the 90s, the CNN developed by LeCun et al at AT&T/Bell Labs was deployed by NEC and was reading more than 10% of all checks in the US.
* See 2003 paper by Simard, Steinkraus, and Platt "Best Practices for Convolutional Neural Nets" in *ICDAR 2003* for more examples of CNNs used for OCR and handwriting recogonition deployed by Microsoft
* For more an in-depth history of CNNs, see 2010 paper by LeCun, Kavukcuoglu, and Farabet "Convolutional networks and applications in vision." *Proceedings of 2010 IEEE ISCAS (International Symposium on Circuits and Systems)*
* CNNs were also used to win many contests. The current intensity of commercial interest in deep learning began when Krizhevsky et al (2012) won the ImageNet object recognition challenge. 
* ...But CNNs had already been used to win other ML and computer vision contests (with less impact) for years earlier.
* CNNs were some of the first working deep networks trained with backprop.
* It's not entirely clear why CNNs succeeded when general back-propagation networks were considered to have failed.
* It may simply be that CNNs were more computationally efficient than fully-connected networks--so it was easier to run multiple experiments with them and tune their implementation and hyperparameters.
* Larger networks also seem to be easier to train.
* With modern hardware, large fully connected networks appear to perform reasonably on many tasks, even when using datasets and activation functions that were available and popular during the earlier times when fully connected networks were believed to not work well.
* Possibly, **the primary barriers to the success of neural networks were *psychological*.** i.e., Practitioners did not expect neural networks to work, so they did not make a serious effort to use neural networks.
* Whatever the case, it is fortunate that CNNs performed well decades ago. **In many ways, CNNs carried the torch for the rest of deep learning** [during the lean years of the ANN winter]. And then, CNNs paved the way to the acceptance of neural networks in general.

