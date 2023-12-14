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
* p. 171 The largest difference between the linear models we have seen so far and neural networks is that the nonlinearity of an ANN causes most interesting loss functions to become nonconvex.
	* i.e., JH: A convex function in this case means a function that has a global optimum (max--or in the case of a loss function, a minimum) that is relatively easy to find. 
	* Thus, ANNs are usually trained by using an iterative, gradient-based optimizer that merely dives the cost function to a very low value; instead of the linear equation solvers used to train linear regression models. This also means that the convex optimization algos with global convergence usd to train logistic regressions and SVMs are not available.
* Convex optimization converges starting from any initial parameters in theory; in practice, it is robust but can encounter numerical problems. 
* SGD applied to nonconvex loss functions has no such convergence guarantee and is sensitive to the values of the initial parameters.
* p. 172 For FFN, it is important to set as initial values: 
	* Weights to small random values
	* Biases to zero or small positive values
* The iterative gradient-based optimization algorithms used to train FFN are examined more carefully in Chapter 8.
* For now, the training algo is almost always based on using the gradient to descend the cost function in one way or another.
* The specific algos are improvements and refinements to the ideas of gradient descent, introduced in Section 4.3; more specifically, are most often improvements of the SGD algo introduced in Section 5.9
* We can of course train models such as linear regression and SVM with gradient descent as well. In fact, this is common practice when the training data set is extremely large.
	* From this perspective, training an ANN is not much different from training any other model. 
	* In Section 6.5, we describe how to obtain the gradient using the backprop algo and modern generalizations of backprop.

#### 6.2.1 Cost Functions
* p.172 First, let's review how we choose cost functions for simpler parametric models such as linear models. 
	* In most cases, our parametric model defines a distribution **p(** y&#8407; **|** x&#8407;; **&#952; )**. In this case, we simply use the principle of maximum likelihood; i.e., we use the cross-entropy between the training data and the model's predictions as the cost function.
* Sometimes, we take a simpler approach, where rather than predicting a complex probability distribution over y&#8407;, we merely predict some sub-statistic of y&#8407; conditioned on x&#8407;.
	* Specialized loss functions enable us to train a predictor of these estimates.
* p.172-173 When training an ANN, we often combine these primary cost functions with a regularization term. Before, we've seen simple versions of regularization applied to linear models in section 5.2.2.
	* The weight decay approach used for lienar models is also directly applicable to deep neural networks and is among the most popular regularization strategies.

##### 6.2.1.1 Learning Conditional Distributions with Maximum Likelihood

* p.173 Most modern neural networks are trained using maximum likelihood. This means that the cost function is simply the NLL (negative log-likelihood) aka the cross-entropy between the training data and the model distribution. This cost function is given by Eq. 6.12: 
	* J(**&#952;**) = -E<sub>x&#8407;,y&#8407;~p<sub>data</sub></sub>log p<sub>model</sub>( y&#8407; | x&#8407; ) 
* The specific form of the cost function changes from model to model, depending on the specific form of log p<sub>model</sub>. The expansion of Eq 6.12 typically yields some terms that do not depend on the model parameters and may be discarded. 
* p.173 An advantage of this approach of deriving the cost function from maximum likelihood is that it removes the burden of designing unique cost functions for each model.
	* Specifying a model p( y&#8407; | x&#8407; ) automatically determines a cost function log p ( y&#8407; | x&#8407; ).
* One recurring theme throughout ANN design is that the gradient of the cost function must be large and predictable enough to serve as a good guide for the learning algorithm.
	* Functions that saturate (become very flat) undermine this objective because the make the gradient become very small. 
	* In many cases, this happens because the activation functions used to produce the output of the hidden units or the output units saturate.
	* The NLL (negative log-likelihood) helps to avoid this problem for many models.
* p.174 One unusual property of the cross-entropy cost used to perform maximum likelihood estimation is that it usually does not have a minimum value when applied to the models commonly used in practice.
	* See more on regularization etc. in Chapter 7.  

##### 6.2.1.2 Learning Conditional Statistics
* p. 174 Instead of learning a full probability distribution p( y&#8407; | x&#8407;; **&#952;** ), we often want to learn just a single conditional statistic of y&#8407; given x&#8407;.
	* e.g., we might use the predictor f( x&#8407; ; **&#952;** ) to predict **the mean value** of y&#8407;.
* If we use sufficiently powerful neural network, we can think of the neural network as being able to represent any function f from a wide class of functions, with this class being limited only by features such as continuity and boundedness.
* p. 174 Some discussion of functionals and calculus of variations. Note: a functional is just a mapping from a transformation/function (as the domain) to &#8477;<sup>1</sup> (as the co-domain).
* p. 175 Explores derivation of MSE (mean squared error) and MAE (mean absolute error) from calculus of variations. And why these stats are less popular than cross-entropy cost function.

#### 6.2.2 Output Units
* p. 175 the choice of cost function is tightly coupled with the choice of output unit.
* Most of the time, we simply use the cross-entropy between the data distribution an the model distribution. the choice of how to represent the output then determines the form of the cross-entropy function.
* The linear, sigmoid, and softmax output units explored in section 6.2.2 are primarily used for output layers. However, they and similar neurons can be used in hidden layer as well.
	* p. 176 Section 6.2.2.1 Linear Units for Gaussain output distributions
	* p. 176 Section 6.2.2.2 Sigmoid Units for Bernoulli Output Distributions
		* p. 177 logits are defined as a *z*-variable defining probabliity distributions over binary variables.

##### 6.2.2.3 Softmax Units
* p. 178 Section 6.2.2.3 Softmax Units for Multinoulli output distributions
* p. 181 From a neuroscientific point of view, we might interpret the softmax as a way to create a form of competition between the neurons that participate in it; the softmax outputs always sum to 1 so an increase in the value of one unit necessarily corresponds to the decrease the value of the others. aka zero-sum as inputs to the target neuron.
	* This is analogous to the inhibition that is believed to occur between different neurons that both feed into the same destination neuron for cells within the cortex.
	* At the extreme, aka when one of the inputs is nearly 1 and the inputs of the other parallel neurons is close to 0, this is like a form of **winner-take-all**.
* p. 181-182. The name 'softmax' can be somewhat confusing. The function is more closely related to the `arg max` function than the `max` function. 
	* The term 'soft' derives from the fact that the softmax function is continuous and differentiable. The `arg max` function with its results represented by a one-hot vector, is not continuous or differentiable.
	* Thus, the softmax function provides a *softened* version of the harsh `arg max`.
	* The corresponding soft version of the maximum function is softmax(z&#8407;)<sup>transpose</sup>z&#8407;.
	* A more accurate name is probably 'soft arg max' rather than 'softmax'; but *softmax* is the convention at this point.

##### 6.2.2.4 Output Units other than Linear, Sigoid, or Softmax
* p.182-185 Other types of output units 

#### 6.3 Hidden Units
* p.185-186 The design of hidden units is an extremely active area of research; there are not many definitive guiding theoretical principles (as of 2016). 
* In general ReLUs are a good starting point for hidden units.
* Some of the following hidden unit types suggested below are not actually differentialble at all input points. e.g., for a ReLU, the rectified linear function of g(z) = max { 0 , z } is not differentiable at the value z =0; it has a 'kink' sharp angle.
	* However, we still choose to use g(z) rectified linewar model b/c gradient descent still works *generally* well enough to kee using ReLU
* Why is it ok to minimize cost functions like ReLU which are *not* differentiable and continuous? See hilly topology function in Figure 4.3, p. 81. Goal is to find a "pretty good" local minimum, not necessarily to find the absolute global minimum.
	* See Chapter 8 for more discussion on this.
	* We accept ReLU's shortcomings as a differentiable, smooth, continuous function because we do not actually expect training to actually reach where g'(x) = 0.It is acceptable for the minima of the cost function to correspond to points with undefined gradient.
	* Even if a hidden unit is non-differentiable sometimes, that only occurs in realtively small parts of its domain. i.e., Hidden units that are note differentiable are usually non-differentiable at only a small number of points.
* In general, a function g(z) has a left derivative defined by the slope of the function immediately to the left of z aka *g'<sub>left</sub>(x)*; and the right derivative defined by the slope of the function immediately to the right of z aka *g'<sub>right</sub>(x)*.
	* A function is differentiable at z only iff both the left derivative and right derivative are defined and are equal to each other.
* The functions used in the context of neural networks usually have defined left derivatives and defined right derivatives. So even though there is a "kink" at z = 0 making the function not smooth and differentiable at z = 0, g(z) *is* differentiable to the left of z = 0 and to the right of z = 0.
	* In the example of the softmax activation function g(z)--aka **g(z) = max{0,z}**-- the left derivative *g'<sub>left</sub>'(x)=0* at z=0 and the right derivative *g'<sub>right</sub>(x)=1* at z=0.
	* **Software implementations of ANN training usually return *one* of the one-sided derivatives rather than reporting that the derivative is undefined or erroring out.** aka, *g'(x)=0* or *g'(x)=1*.
* p.186-187 Some theoretical justifications. But the bottom line: totally ok to ignore the nondifferentiability of hidden unit activations and pragmatically implement as effectively differentiating cleanly at z=0.

##### 6.3.1 ReLUs and their generalizations

* p.187 ReLUs are easy to optimize because they are so similar to linear units. Again, the only difference between a vanilla linear unit and a ReLU is that a ReLU outputs 0 across half its domain.
* This means that derivatives through a ReLU **remain large whenever the unit is active**. 
* Also, the gradients are not only large but *consistent*.
* The 2nd derivative *g''(x)* of the rectifying operation is 0 almost everywhere and the derviative of the rectifying operation is 1 everywhere teh unit is active.
	* This means that the gradient direction is far more useful for learning than it would be with activation functions which might introduce 2nd-order effects.
* ReLUs are typically accept vectors with an affine line (aka has a bias *b* such that it does not cross the origin). **h** = **g(**`W`<sup>transpose</sup>x&#8407; + b&#8407;**)**
* When initializing the parameters of an affine transformations, it can be good practice to set all the biases *b* to a small positive value, such as 0.1.
	* Doing so makes it more likely that the ReLUs will have some initial activation for most inputs to the training set and will allow derivatives to pass through.

##### Generalizations from the vanilla ReLU
* p.187 - One drawback to ReLUs is that they cannot learn via gradient-based methods when a training example leads to an activation of exactly 0. Several generalizations / variants of ReLU work around this problem by ensuring that g(z) is differentiable everywhere.
* p.187-188. When a slope *alpha<sub>i</sub>* is nonzero and z is less than zero (aka z is negative), we have a small output value for *h* such that *h<sub>i</sub>* = g(z&#8407;, **alpha**)<sub>i</sub> = **max(** 0 , z<sub>i</sub> **)** + *alpha<sub>i</sub>* **min(** 0 , z<sub>i</sub> **)**:
	1. Absolute value rectification (Jarrett et al, 2009)
	1. Leaky ReLU (Maas et al, 2013)
	1. Parametric ReLU aka *PReLU* (He et al, 2015) 
* p.188. Goodfellow et al in 2013 proposed **Maxout Units** as another variant / generalization. These units separate the activation into *k* different subcomponents.
	* Maxout Units provides a way to learn a piecewise linear function that reponds to multiple directions in the input x&#8407; spacje.
	* A maxout unit can learn a piecewise linear convex function with up to *k* pieces.
	* A maxout unit can *learn the activation function itself* rather than just the relationship between units.
	* Maxout units also show resistanct to the phenonmenon of **catastrophic forgetting**.
* ReLUs and their variants are based on the principle that models are easier to optimize if an activation function is close to a linear function.

#### 6.3.2 Logistic Sigmoid and Hyperbolic Tangent
* p. 189 The ReLU function was first studied in biology in the last 1960s but were not really introduced to ANN research until 2009-2011. For a good history on this, see [this article](https://machinelearningmastery.com/rectified-linear-activation-function-for-deep-learning-neural-networks/).
	* Sigmoid function mostly used in the 90s.
	* Late 90s through first decade of 2000s - tanh aka hyperbolic tangent.
* **Sigmoid function** related to the Gaussian normal distribution: *g(z) = &#963;(z)* aka lowercase sigma.
* **Hyperbolic tangent** *aka* tanh: *g(z) = tanh( z )*






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



## Notes for Nueva Jan 2024
* History of computing link by Steve Furber, one of the early ARM chip designers. Published March 2017. ['Microprocessors: the engines of the digital age.'](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5378251/)

### More notes on humanities
* Dec 11. quick history of 1944 neural networks proposed, early researchers moved to MIT in 1952, Minsky and Papert topped it 1968 etc in this [Intro to Liquid Neural Networks](https://hackernoon.com/an-introduction-to-liquid-neural-networks-nt5c33t7)




***

### Section 6.5: Overview of Backprop and other Differentiation Algorithms
#### 6.5.1: Introduction to Computational Graphs
#### 6.5.8: Complications (aka practical considerations) wrt simple theoretical narrative about backprop
#### 6.5.9: Differentiation outside the Deep Learning Community
* Relevant to unrolling RNNs in chapter 10
### Section 6.6: Historical Notes p. 220
* 'Feedforward networks can be seen as eﬃcient nonlinear function approximatorsbased on using gradient descent to minimize the error in a function approximation. From this point of view, the modern feedforward network is the culmination of centuries of progress on the general function approximation task.

#### Calculus in the 1600s, Cauchy approximations in the 1800s
* From Leibniz (1676) and L’Hôpital (1696), the calculus chain-rule that underlies backprop was invented in the 1600s. 
* 'Calculus and algebra have long been used to solve optimization in the closed form.' But gradient descent was not introduced as a technique for iteratively approximating the solution numerically (not analytically) until Cauchy (1847) and others in the mid-19th century.' p. 221
* 'Beginning in the 1940s, these function approximation techniques were used to motivate early machine learning models such as the perceptron. However, the earliest models were based on linear models.
* 'Critics including Marvin Minsky pointed outseveral of the ﬂaws of the linear model family, such as its inability to learn the XOR function, which led to a backlash against the entire neural network approach.
* 'Learning nonlinear functions required the development of the MLP (multilayer perceptron) plus the computing resources to compute a gradient through them.'
* 'Efficient applications of the chain rule based on dynamic programming began to appear in the 1960s and 1970s, mostly for control applications but also for sensitivity analysis.
* 'Werbos (1981) proposed applying these techniques to training ANN artificial neural networks.

#### Popularization of backpropagation in the 1980s
* Various people rediscovered and put into practice within silicon: Yann LeCun (1985), Parker (1985), the *Nature* article 'Learning representations by back-propogating errors' by Rumelhart, Hinton, and Williams (1986)
* 'Parallel Distributed Processing' by Rumelhart, McClelland, and the PDP Research Group (1986) was a critical book. In the chapter 'Learning internal representations by error propagation' by Rumelhart, Hinton, and Williams, the results of these early successes with backpropagation popularized these technique more broadly.
* The ideas put forward the PDP book, esp. those of Rumelhart and Hinton, go much beyond backprop. They include crucial ideas about the possible computational implementation ofseveral central aspects of cognition and learning, which came under the name *connectionism* because of the importance this school of thought places on theconnections between neurons as the locus of learning and memory.
* A key idea was the notion of **distributed representation** in an important chapter in the PDP book by Geoff Hinton and [Terry Sejnowski](https://en.wikipedia.org/wiki/Terry_Sejnowski) (Princeton, Johns Hopkins, CalTech, Salk Institute). Co-invention of the Boltzmann machine, and his PhD advisor was John Hopfield of the ['Hopfield Network'](https://en.wikipedia.org/wiki/Hopfield_network). 'Learning and relearning in Boltzmann machines', from Vol 1., Chapter 7 p. 282-317 of *Parallel Distributed Processing*
* Following the success and popularity of the backprop algorithm in the mid-1980s, neural network research gained momentum and reached a peak of AI spring in the early 1990s. 
* 'Afterwards, the AI winter returned for neural networks and other machine learning techniques became more popular until the modern deep learning renaissance that began in 2006 with deep belief networks.'
* GBC: 'The core ideas behind modern feedforward networks have not changed substantially since the 1980s. p.221
	* The **same** back-propagation algorithm and the **same approaches to gradient descent** are still in use. 
	* Most of the improvement in neural network performance from 1986 to 2015 can be attributed to two factors. 
		1. First, larger datasets have reduced the degree to which statistical generalization is achallenge for neural networks.
		1. Second, neural networks have become much larger, because of more powerful computers and better software infrastructure.

#### 1990s–late 2000s Algorithmic Improvements: (a) Cross-Entropy Loss and (b) ReLUs
*A small number of algorithmic changes have also improved the performance of neural networks noticeably. p.222*

##### (a) Rise of Cross-Entropy Loss
* 'One of these algorithmic changes was the replacement of mean squared error with the **cross-entropy family of loss functions**.
	* Mean squared error was popular in the 1980s and 1990s but was gradually **replaced by cross-entropy losses** and the **principle of maximum likelihood** as ideas spread between the statistics communityand the machine learning community. 
	* The use of cross-entropy losses greatly improved the performance of models with sigmoid and softmax outputs, which had previously suﬀered from saturation and slow learning when using the mean squared error loss.

##### (b) Rise of Rectified Linear Units
* 'The other major algorithmic change that has greatly improved the performance of feedforward networks was the replacement of sigmoid hidden units with piecewise linear hidden units, such as rectiﬁed linear units. 
* JH: Before the rise of ReLU, *sigmoid functions* were used for the neurons in the hidden layers. For example, logistic / sigmoid activation functions.
* 'Rectiﬁcation using the `max{0,z}` function was introduced in early neural network models and dates back at least as far as the cognitron and neocognitron (Fukushima, 1975, 1980). 
* 'These early models [from the 1970s] did *not* use rectiﬁed linear units but instead applied rectiﬁcation to *nonlinear functions*.
* 'Despite the early popularity of rectiﬁcation, it was largely replaced by sigmoidsin the 1980s, perhaps because sigmoids perform better when neural networks are very small. 
* 'As of the early 2000s, rectiﬁed linear units were avoided because of a somewhat superstitious belief that activation functions with nondiﬀerentiable points must be avoided. 
* 'This began to change in about 2009. Jarrett et al. (2009) observed that “using a rectifying nonlinearity is the single most important factor in improving the performance of a recognition system,” among several diﬀerent factors of neural network architecture design.'
* 'For small datasets, Jarrett et al. (2009) observed that using rectifying non-linearities is even more important than learning the weights of the hidden layers.
* 'Random weights are suﬃcient to propagate useful information through a rectiﬁed linear network, enabling the classiﬁer layer at the top to learn how to map diﬀerent feature vectors to class identities.'
* 'When more data is available, learning begins to extract enough useful knowledgeto exceed the performance of randomly chosen parameters. Glorot et al. (2011a) showed that learning is far easier in deep rectiﬁed linear networks than in deepnetworks that have curvature or two-sided saturation in their activation functions.'
* 'Rectiﬁed linear units are also of historical interest because they show thatneuroscience has continued to have an inﬂuence on the development of deeplearning algorithms. Glorot et al. (2011a) motivated rectiﬁed linear units from biological considerations.
* The half-rectifying nonlinearity was intended to capture these properties of biological neurons: (1) For some inputs, biological neurons are completely inactive. (2) For some inputs, a biological neuron’s output is proportional to its input. (3) Most of the time, biological neurons operate in the regime where they are inactive (i.e., they should have sparse activations).

#### From 2006 onwards starting with Deep Belief Networks
* 'When the modern resurgence of deep learning began in 2006, feedforward networks continued to have a bad reputation. From about 2006 to 2012, it was widely believed that feedforward networks would not perform well unless they were assisted by other models, such as probabilistic models. 
* 'It is now known that with the right resources and engineering practices, feedforward networks perform very well. Today, gradient-based learning in feedforward networks is used as a tool to develop probabilistic models, such as the variational autoencoderand generative adversarial networks, described in Chapter 20. 
* 'Rather than being viewed as an unreliable technology that must be supported by other techniques, gradient-based learning in feedforward networks has been viewed since 2012 as a powerful technology that can be applied to many other machine learning tasks. 
* 'In 2006, the community used unsupervised learning to support supervised learning, and now, ironically, it is more common to use supervised learning to support unsupervised learning. Feedforward networks continue to have unfulﬁlled potential. 
* 'In the future, we expect they will be applied to many more tasks, and that advances in optimization algorithms and model design will improve their performance even further. This chapter has primarily described the neural network family of models. In the subsequent chapters, we turn to how to use these models--how to regularize and train.'


