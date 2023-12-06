---
layout: ../../layouts/MarkdownPostLayout.astro
title: 'Goodfellow (GBC) Chapter 6'
LastUpdatedDate: 2023-12-28
CreatedDate: 2023-10-28
description: 'Deep Feedforward Networks, including history from 1980s onwards in Section 6.6'
author: 'Jeff'
tags: []
---


**Deep Learning (2016)** 
* Ian Goodfellow, Yoshua Bengio, and Aaron Courville
* GBC
* See also [Learning from Data](www.amlbook.com) book by **Abu-Mostafa, Magdon-Ismail, and Lin (aka AML)**. Relevant chapters: 
	* Chapter 2 (training set, test set, generalization, VC dimension, Bias vs. Variance; most relevant to GDB Chap 5) 
	* Chapter 3 (Linear Model-- most relevant to GDB Chapter 6)
	* Chapter 4 (Overfitting, Regularization, Weight Decay, and Validation Dataset)
## Chapter 6: Deep Feedforward Networks p. 163
* Basic definitions p.163-165: **depth** referring to number of hidden layers between input layer and output layer. **width** of each layer refers to how many dimensions can be managed. Each artificial neuron can be referred to as a **unit**.
* p.164 Rather than thinking of the layer as representing a single vector-to-vector function, we can also think of the layer as consisting of many units that act in parallel. Each unit can be thought of as a vector-to-scalar function; aka, multiple values for input to a neuron and a output a single activation value.
* **Important note about *asterisk* notation.** For a given function **g(x)**, the notation **g<sup>*</sup>(x)** indicates the optimal values of x such that dg/dx = g'(x) = 0. i
	* For example, when we engage in deep learning, we are trying to iteratively optimize the objective function **J(&#952;)** such that **J(&#952;)** gets as close as possible to **J<sup>*</sup>(&#952;)**. 
	* Aka **J(&#952;)** &#8776; **J<sup>*</sup>(&#952;)** 

### Extending linear models to represent nonlinear functions
* p.164 To extend linear models to represent nonlinear functions of x&#8407; , we can apply the linear model not to x&#8407; itself but instead to a transformed input phi &#966;(x&#8407;), where phi is a nonlinear transformation
* Equivalently, we can apply the kernel trick from Section 5.7.2. to obtain a nonlinear learning algorithm based on implicitly applying the phi &#966; mapping. 
* We can think of &#966; as providing a set of features describing x&#8407;, or as providing a new representation x&#8407;.  

### Three options of how to choose the mapping &#966;
* p. 165 Technically, the mapping phi &#966;: **X**&#8594;**Y**. Exactly equivalent to saying &#966;: &#8477;<sup>m</sup> &#8594; &#8477;<sup>n</sup>.
	* *Input* -- x&#8407; &#8712; domain **X** which is a real valued *m*-dimensional space aka &#8477;<sup>m</sup>. 
	* *Output* -- y&#8407; &#8712; co-domain **Y** which is a real valued *n*-dimensional space aka &#8477;<sup>n</sup>. 

1. **Option 1 -- Choose a very generic &#966;: X&#8594;Y.**
	* i.e., create a function phi &#966; that maps from an infinite-dimensional domain to a finite-dimensional co-domain, aka &#966;: &#8477;<sup>&#8734;</sup> &#8594; &#8477;<sup>n</sup>. 
	* This is implicitly what kernel machines do based on the RBF kernel (radial based function). See kernel machines on p. 139.
	* If &#966;(x&#8407;) is high-dimensional enough, it has enough model capacity to describe the data-generating process suggested by the training dataset. i.e., we will have done a good job minimizing training error.
	* However, if the capacity is too high, we will have overfitting problems. i.e., When we apply this model to new examples from the test dataset, it will have overlearned the training dataset and we will see generalization errors. The usual problems described from Section 5.2 (p.107).
1. **Option 2 -- Use symbolic AI approaches to painstakingly construct &#966;: X&#8594;Y.**
	* What GBC calls "Manually engineering &#966;()"
	* Before we invented deep learning, the hand-crafted approach was the most common strategy. Sounds like symbolic AI to me....
	* i.e., Manual engineering of &#966;(x&#8407;) required decades of human effort to learn each separate task.
	* Different hunan practitioners specialized in different domains such as speech recognition, computer vision, etc.
	* There was litte transfer between different domains.
1. **Option 3 -- Use deep learning to *learn* mapping &#966;** that is a composite of smaller successive functions f<sub>1</sub>()...f<sub>k</sub>()
	* *Chain rule* -- **&#966;(x&#8407;)** = y&#8407; = **f<sub>k</sub>(f<sub>...</sub>(f<sub>2</sub>(f<sub>1</sub>(x&#8407;))))** *aka* Jeff's repeated invocation of successive functions **f()**. That is, we can decompose the overall single-step function **&#966;()** into successive smaller functions **f<sub>1</sub>()...f<sub>k</sub>()**; one function f() for each hidden layer.

#### Diving more into Option 3 above
* p. 165 In the deep learning approach, we have a model y = f(x&#8407;; **&#952;**, w&#8407;).
	* In this context, theta **&#952;** refers to the set of parameters that are optimized over time to learn the proper construction of &#966;(). *JH: not 100% sure about this part*
		* **&#952;** is generally a vector that stores as many values as needed. *JH: not 100% sure about this part*
	* w&#8407; is another vector parameter that maps from &#966;(x&#8407;) to the ultimate output in **Y**. *JH: not 100% sure about this part*
* Of the 3 options outlined above on p.165, Option 3 Deep Learning is the only one that gives up the convexity of the training problem; however, the benefits outweight the costs.
* In this approach, we parametrize the representation as &#966;(x&#8407;;**&#952;**) and use the optimization algorithm to find the value for **&#952;** that best corresponds to a good representation.
* If we wish, this approach can capture the benefit of the first approach by being highly generic--we do so by using a very broad family of functions &#966;(x&#8407;;**&#952;**). 
* Deep learning can also capture the benefits of option 2 above (manual construction).
	* Human practitioners can encode their knowledge to help generalization by designing families &#966;(x&#8407;;**&#952;**) that they expect can perform well.
	* Using DL, now the human practioner can focus on finding the right *general family of functions* and then letting SDG etc find the ideal function (or ideal enough). 
	* Whereas in a pure version of Option 2, the human might have to manually find the perfect function which is a lot more time-consuming; indeed it may be effectively impossible b/c the search space is so large.

***
### Quick overview of the rest of Chapter 6
* Simple example of a feedforward network
* Address each of the design decisions needed to deploy a feedforward network
* Review the basics of gradient-based learning.
* Choice of activation function (logistic sigmoid, hyperbolic tangent, softmax, etc.)
* Quick intro to backpropagation

***


### Example: Learning Exclusive OR (XOR)
* What is theta **&#952;** in this context? p. 167. "Now we must choose the form of our model, f(x&#8407;, **&#952;**). Suppose that we choose a linear model, theta **&#952;** consists of a vector w&#8407; and a single scalar bias b. Vector w&#8407; contains multiple weights.
* We can minimize objective function J(&#966;) in closed form with respect to w&#8407; and b using the normal equations. 
* Talks about Minsky's 1969 critique of learning XOR, and how it's solved by having at least 1 hidden layer. So now there is not a single function, but two functions f<sub>1</sub> and f<sub>2</sub>.
* p.168 classic diagram of learning XOR Figure 6.1
* p.168 definition of **ReLU** aka **rectified linear unit**. Relevant papers were only published 2009-2011.
* p.169 Figure 6.3: Diagram of activation function 
	* The ReLU function is the default activation function recommended nowadays for most feedforward ANNs. Applying this function to the output of a linear transformation yields a nonlinear transformation. 
	* The function remains very close to linear, however, in the sense that it is a piecedwise linear function with 2 linear pieces. 
	* Because ReLUs are very nearly linear, they preserve many of the properties that make linear models easy to optimize with gradient-based methods.
	* They also preserve manhy of the properties that make linear models generalize well.
	* A common principle throughout computer science
* p.169 Figure 6.2: Two alternate ways of drawing an ANN diagram
	* The more verbose diagram on the right. In this style, every unit (*aka* neuron) is drawn as a distinct node in the graph. While this style is nicely unambigous and easier to read, it can require too much paper to represent more complex ANNs.
	* The more concise diagram on the left. In this style, we draw a circular node in the graph to represent the activation of an entire layer of neurons.
		* Sometimes we annotate the edges in this graph with the name of the parameters that describe the relationship between two layers.
		* Here, we use capital letter W to indicate that a matrix **W** contains the weight values between the input layer and the hidden layer. It's not just a scalar.
		* There is a vector w&#8407; that contains the activations between hidden layer and the final output layer.
		* We typically omit the intercept parameters associated with each layer when labeling this kind of drawing.
	* Note that the ANN expressed in Figure 6.2 solves the XOR problem. It has a total of 5 neurons--2 input neurons; 2 neurons in the hidden layer; and 1 output neuron.
* p.166-167. How do we solve XOR? 
	* Desired output for an XOR ann: Given 2 input neurons which only have 2 binary states (1 or 0), we want to learn a function that only outputs 1 when *exactly one* of the input neurons = 1. 
		* i.e., 0,0; 1,1 --> output=0
		* 1,0; 0,1 --> output=1
	* First let us demonstrate the naive implementation using linear regression and MSE (Mean Squared Error), which results in weights = 0 and b = 1/2. 
	* This means the output of the naive regression is always 1/2. We don't want that. In fact, Minsky proved in 1968 that a proper XOR functionality is impossible to train via neural networks; at least one that only has 2 layers..

* p.167 To solve this with a neural network, we need to have a *third*, hidden layer added. To write out equations and diagrams related to the XOR ANN, see Comp Sci notebook #1, November 21, 2023 drawings.
	* We have two functions that run sequentially. First f<sub>1</sub>(x&#8407;) outputs **h**. Then, f<sub>2</sub>(**h**) outputs y. 
	* *Formatting issue:* in above equestions, *h* should have a vector arrow drawn above it, but *h&#8407;* looks weird.

### 11/22 notes
* Pulled out Learning From Data and their alternative take on all this material is excellent and useful. Takes some time to get the math though...

## Notes for Nueva Jan 2024
* History of computing link by Steve Furber, one of the early ARM chip designers. Published March 2017. ['Microprocessors: the engines of the digital age.'](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5378251/)


#### Using a simple feedforward network to solve XOR
* p. 167 A simple feedforward network is able to learn a different feature space in which a linear model is able to represent the solution.
* Specifically, we will introduce a simple FFN with one hidden layer containing 2 hidden units. See diagram drawn in JH Comp Science #1, 11/21/2023; p.169, Figure 6.2.
* This feedforward network has a vector of hidden units **h** that are computed by a function f<sub>1</sub>(x&#8407;; **`W`**,c&#8407;). Where **`W`** is a matrix containing the weights for both neurons h<sub>1</sub> and h<sub>2</sub>.
    * The output of function f<sub>1</sub> is then used for the 2nd, output layer.
    * The output layer is still just a linear regression model which is now applied to **h** rather than the inital input x&#8407;.
* Most ANNs use an affine transformation controlled by learned parameters, followed by a fixed nonlinear function called an activation function.
* We use that strategy here by defining **h** = g(**`W`**<sup>transpose</sup>x&#8407; + c&#8407;) where **`W`** is a matrix that provides the weights of a linear transformation and vector c&#8407; provides the biases.
* Previously, to describe a linear regression model, we used a vector of weights and a scalar bias parameter to describe an affine transformation from an input vector to an output scalar.
* Now, we describe an affine transformation from a vector x&#8407; to a vector **h**, so that an entire vector of bias parameters is needed.
* The activation function g is typically chosen to be a function that is applied element-wise, with each h<sub>i</sub> = g(x&#8407;<sup>transpose</sup>**`W`**<sub>i</sub>+c<sub>i</sub>).
* In modern ANNs, the default recommendation is to use the rectified Linear Unit **ReLU**.
* We can specify the complete network as f(x&#8407;;**`W`**,c&#8407;, w&#8407;, b) = w<sup>transpose</sup>max(
* (End of p. 168)

### Section 6.2 Gradient-Based Learning
* p. 173 The largest difference between the linear models we have seen so far and neural networks is that the nonlinearity of an ANN causes most interesting loss functions to become nonconvex.
	* i.e., JH: A convex function in this case means a function that has a global optimum (max--or in the case of a loss function, a minimum) that is relatively easy to find. 
	* Thus, ANNs are usually trained by using an iterative, gradient-based optimizer that merely dives the cost function to a very low value; instead of the linear equation solvers used to train linear regression models. This also means that the convex optimization algos with global convergence usd to train logistic regressions and SVMs are not available.
* Convex optimization converges starting from any initial parameters in theory; in practice, it is robust but can encounter numerical problems. 
