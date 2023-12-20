---
layout: ../../layouts/MarkdownPostLayout.astro
title: 'Goodfellow (GBC) Chapter 7'
pubDate: 2023-11-15
LastUpdatedDate: 2023-12-28
CreatedDate: 2023-10-28
description: 'Notes from Chapter 7 (Regularization)'
author: 'Jeff'
tags: []
---

**Deep Learning (2016)** 
* Ian Goodfellow, Yoshua Bengio, and Aaron Courville
* GBC
## Chapter 7: Regularization for Deep Learning p. 221
* Simply defined, regularization is any technique or process that allows the **reduction of test error** (aka *generalization error* see notes on Chapter 5) while accepting some increase in training error.
* See also Chapter 5 of ISL (Introduction to Statistical Learning 2021 by Tibshirani et al). PDF available in Box
* See also quick overview of Regularization concepts in GBC Section 5.2.2, such as very basic treatment of "generalization, underfitting, overfitting, bias, variance, and regularization." p. 221
	* On GBC p. 107 note that '**generalization error** is exactly synonymous with **test error**' from first page of Section 5.2
* 'Regularization adds terms to the objective function which can be thought of as extra constraints and penalities.
* 'Sometimes these constraints/penalties are meant to improve performance on the test set. 
* 'Sometimes these constraints/penalties **are designed to encode specific kinds of prior knowledge**.
* 'Sometimes these constraints/penalties are meant to improve the generalization of a model so that it does not overfit on a simple objective.
* 'Finally, regularization includes *ensemble methods* which combine multiple hypotheses to explain training data' p.222
* In the context of deep learning, *most regularization strategies are based on regularizing estimators*.
	* **Regularizing an estimator works by trading increased bias for reduced variance.**
	* An effective regularizer is one that makes a profitable trade by significantly reducing variance while not overly increasing bias.
* Per Chapter 5, there were 3 regimes:
	1. Excluding the true data-generating process (aka *underfitting* and *inducing bias*)
	1. Correctly/accurately matching the data-generating process
	1. *Including* the true data-generating process *but* also matching many other generating processes (aka *overfitting*)
		* In this overfitting regime, variance rather than bias dominates the estimation error
* The goal of regularization is to move from the 3rd regime above to the 2nd regime.
* Some archaelogy. **J() = objective function**. From GBC p.79, synonyms for objective function include:
	* **cost function**
	* **loss function**
	* **error function**
* Also from p.79, "We often denote the value that minimizes or maximizes a function with a superscript *. For example, we might say x&#8407;<sup>\*</sup> = arg min f(x&#8407;)." i.e., x&#8407; refers to when f'(x&#8407;) = 0 and there is a minimum in the derivative df/dx.  
* Where is the first instance of theta **&#952;** ?
	* p.119 Point estimation from Section 5.4.1. True value of a parameter is denoted by **&#952;**. In contrast, the *estimate* of the value of the parameter is with **&#952;-hat**. And since both the regular and hat versions of theta are vectors, they can contain many values for the parameter.
	* p.165 Intro to Chap6 on Deep FeedForwward networks. Third of 3 options on mapping of function phi aka &#966;. 'We now have a parameters **&#952;** that we use to learn &#966; from a broad class of of functions. And also a vector w&#8407; that contains all the individual `weight` values that map from &#966;(x&#8407; ) to the final output.' 


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

