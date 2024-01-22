---
layout: ../../layouts/MarkdownPostLayout.astro
title: 'Learning Plan on RNN, Autoencoders, etc.'
LastUpdatedDate: 2024-01-23
CreatedDate: 2023-10-28
description: 'Study plan as of February, 2024'
author: 'Jeff'
tags: []
---

***
## Next items and other interesting notes
1. Finish GBC chapter 8 on optimization
1. Reread Introduction from p. 1 - 26 on history of AI / ML. Note this from p. 4 of introduction:
	1. The quintessential example of a representation learning algorithm is **the autoencoder**. 
	1. An autoencoder is the combination of an **encoder function**, which converts the input data into a diﬀerent representation, and a **decoder function**, which converts the new representation back into the original format. 
	1. Autoencoders are trained to preserve as much information as possible when an input is run through the encoder and then the decoder, but they are also trained to make thenew representation have various nice properties. 
	1. Diﬀerent kinds of autoencoders aim to achieve diﬀerent kinds of properties.
1. Quick skim of Chapters 11 & 12: Practical Methodology & Applications
1. Chapter 11, focus on 
	1. Section 11.4 Selecting Hyperparameters p. 415-424
1. Chapter 12, focus on
	1. 12.1 Large-Scale Deep Learning p. 431-440
	1. 12.4 NLP, esp. Section 12.4.5.1 Attention Mechanism p. 462 and 12.4.5.2 Historical Perspective on Natural Language p.464
	1. 12.5.1.1 Exploration vs. Exploitation p. 468 in context of bandits and recommender systems
1. Skip Chap 13 on Linear Factor Models
1. Go straight to Chap 14 on Autoencoders

***
## Then after GBC is finished
1. Read Cho Bengio paper 1 below from 2014
1. Read Cho Bengio paper 2 below from 2014
1. Consolidate histories and add to AI-Timeline
	1. From GBC Introduction chapter
	1. Chapter 9 CNNs on neuroscientific basis / CNNS on history of deep learning sections 9.10 and 9.11
	1. NLP historical perspective from Chapter 12 Applications, p.464

***
## Papers
* *Learning Phrase Representations using RNN Encoder–Decoder for Statistical Machine Translation* by Cho, Bahdanau, Bougares, Schwenk, and Bengio 2014a. [arXiv link](https://arxiv.org/abs/1406.1078) and [PDF](https://arxiv.org/pdf/1406.1078.pdf)
* *On the Properties of Neural Machine Translation: Encoder–Decoder Approaches* by Cho, van Merrienboer, Bahdanau, and Bengio 2014b. [arXiv link](https://arxiv.org/abs/1409.1259) and [PDF](https://arxiv.org/pdf/1409.1259.pdf)

***
**Deep Learning (2016)** 
* Ian Goodfellow, Yoshua Bengio, and Aaron Courville
* GBC
## Chapter 10: Sequence Modeling: RNNs and Recursive Nets
* RNNs (first defined by Rumelhart et al, 1986a) are a family of neural networks for processing sequential data. Much as a CNN specializes in a grid of values **`tensor X`** such as a 2-D image, an RNN is specialized at processing a sequence of vectors **v<sub>1</sub>**...**v<sub>n</sub>**. p.367
* Most RNNs can process sequences of variable length.

### Parameter sharing
* Parameter sharing makes it possible to extend and apply the model to exampels of different lengths and generalize across them. Example of 2 different sentences: "I went to Nepal in 2009" vs "In 2009, I went to Nepal". A simple fully-connected feedforward ANN that is trained to discriminate between these two sentences would eventually converge such that all the rules of the language would have to be learned for each word position.
* In contrast, a RNN shares the same parameter weights across several time steps.

### Explanation of why a 1-D CNN is shallow while a RNN is a deeper representation p. 368
* 'A convolution operation allows a CNN to share parameters across time but is shallow.'
* 'The output ofconvolution is a sequence where each member of the output is a function of asmall number of neighboring members of the input.'
* A RNN shares parameters in a different way.
* **'Each member of the output is a function of the previous members of the output.'**
* 'Each member of the output is produced using the same update rule applied to the previous outputs.'

### Unfolding Computational Graphs p.369
* See diagram in JH Comp Notebook #1.
* 'A computational graph is a way to formalize the structure of a set of computations,such as those involved in mapping inputs and parameters to outputs and loss.' p. 369
* General introduction to computational graphs is in Section 6.5.1. 
	* Each **node** in the graph represents a variable. p. 198
		* The variable may be scalar valued, vector-valued, matrix-valued, tensor-valued, or even some other type.    
	* Each **edge** is called an **operation**. An operation is just a simple function that can output a single output variable. Remember, that variable can be tensor of any rank so you can think of it as a multidimensional array of arbitrary rank and dimension. 
	* Generalities that can come from applying the chain rule in calculus.
	* This leads to recursive application of the chain rule to derive the backpropagation algorithm.
* Classical physics model of a very simple dynamic system across time from `t=0`






