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
1. Simply defined, regularization is any technique or process that allows the **reduction of test error** (aka *generalization error* see notes on Chapter 5) while accepting some increase in training error.
1. See also Chapter 5 of ISL (Introduction to Statistical Learning 2021 by Tibshirani et al). PDF available in Box
1. See also quick overview of Regularization concepts in GBC Section 5.2.2, such as very basic treatment of "generalization, underfitting, overfitting, bias, variance, and regularization." p. 221
	* On GBC p. 107 note that '**generalization error** is exactly synonymous with **test error**' from first page of Section 5.2
1. 'Regularization adds terms to the objective function which can be thought of as extra constraints and penalities.
1. 'Sometimes these constraints/penalties are meant to improve performance on the test set. 
1. 'Sometimes these constraints/penalties **are designed to encode specific kinds of prior knowledge**.
1. 'Sometimes these constraints/penalties are meant to improve the generalization of a model so that it does not overfit on a simple objective.
1. 'Finally, regularization includes *ensemble methods* which combine multiple hypotheses to explain training data' p.222
1. In the context of deep learning, *most regularization strategies are based on regularizing estimators*.
	* **Regularizing an estimator works by trading increased bias for reduced variance.**
	* An effective regularizer is one that makes a profitable trade by significantly reducing variance while not overly increasing bias.
1. Some archaelogy. **J() = objective function**. From GBC p.79, synonyms for objective function include:
	* **cost function**
	* **loss function**
	* **error function**
1. Also from p.79, "We often denote the value that minimizes or maximizes a function with a superscript **(\*)**. For example, we might say x&#8407;<sup>\*</sup> = arg min f(x&#8407;)." i.e., x&#8407; refers to when f'(x&#8407;) = 0 and there is a minimum in the derivative df/dx.  
1. Where is the first instance of theta **&#952;** ?
	* p.119 Point estimation from Section 5.4.1. True value of a parameter is denoted by **&#952;**. 
	* In contrast, the *estimate* of the value of the parameter is with **&#952;-hat**. And since both the regular and hat versions of theta are vectors, they can contain many values for the parameter.

### 7.1 Parameter Norm Penalties
1. Regularization has been used for decades prior to the advent of deep learning. Linear models such as linear regression and logistic regression allow simple, straightforward, and eﬀective regularization strategies. 
1. Many regularization approaches are based on limiting the capacity of models, such as neural networks, linear regression, or logistic regression, by adding a parameter norm penalty &#937;(**&#952;**) to the objective function J. 
1. We denote the regularized version of the objective function with a tilde over the capital J function like so: 
	* J&#771;(**&#952;**; **`X`**, y&#8407;) = J(**&#952;**; **`X`**, y&#8407;) + *alpha \* &#937;(**&#952;**)*
	* the italicized term in Equation 7.1 above is the regularization term: **alpha \* &#937;(&#952;)**
	* And the scalar coefficient term *alpha* is a positive real number. *Alpha* weights the relative contribution of the *norm penalty term &#937;*.
	* If we set alpha = 0, then that cancels out the norm penalty &#937; so that J&#771;() is exactly the same as  J().
1. When our training algorithm minimizes the regularized objective function J&#771; it will decrease *both* the original function J on the training data and to some degree the size of the parameters contained in the vector **&#952;**. 
1. Diﬀerent choices for the parameter norm penalty &#937; can result in diﬀerent solutions being preferred.
1. In section 7.1, we discuss the eﬀects of the various norms when used as penaltieson the model parameters.

### JH Break

1. Before delving into the regularization behavior of diﬀerent norms, we note that for neural networks, we typically choose to use a parameter norm penalty that penalizes *only the **weights** of the aﬃne transformation at each layer and **leaves the biases unregularized***. 
1. The biases typically require less data than the weights to ﬁt accurately. Each weight speciﬁes how two variables interact. Fitting each weight well requires observing both variables in a variety of conditions. 
1. In contrast, each **bias parameter** controls only a *single variable*. This means that we do not induce too much variance by leaving the biases unregularized. 
	* Also, regularizing the bias parameters can introduce a signiﬁcant amount of underﬁtting. 
1. Thus, we use a vector w&#8407; to contain all the **weight parameters** that should be affected by the norm penalty.
	* Meawhile, the vector **&#952;** contains *all* the parameters, including all the weight parameters in w&#8407; (that **are regularized by the norm penalty**) *and* the other (non-weight) parameters that are **not regularized**.

### JH Break

1. In the context of neural networks, it is sometimes desirable to use a separate penalty with a diﬀerent
alpha coeﬃcient for each layer of the network. 
1. Remember, it can be expensive to search for the correct value for several hyperparameters at once. 
1. So it is reasonable and cheaper to use the *same weight decay* at all layers to reduce the size of the search space.

#### 7.1.1 *L<sup>2</sup>* Parameter Regularization
* The most common type of weight decay (p. 227)

#### 7.1.2 *L<sup>1</sup>* Parameter Regularization
* Jacobian and Hessian matrices

### 7.2 Norm Penalties as Constrained Optimization

### 7.3 Regularization and Under-Constrained Problems

### 7.4 Dataset Augmentation

### 7.5 Noise Robustness
* 7.5.1 Injecting noise at the output targets

### 7.6 Semi-Supervised Learning

### 7.7 Multitask Learning

### 7.8 Early Stopping

### 7.9 Parameter Tying and Parameter Sharing
* 7.9.1 CNNs and convultional neural nets p. 247

### 7.10 Sparse Representation

### 7.11 Bagging and other Ensemble Methods

### 7.12 Dropout
* Srivastava et al 2012

### 7.13 Adversarial Training
* GANs (Goodfellow et al 2014) p. 262

### 7.14 Tangent Distance, Tangent Prop, and Manifold Tangent Cluster









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

