---
layout: post
title: What I Learnt From Chapter 6 ("Deep FeedForward Networks") of the Deep Learning Book.
category: posts
---



I am referring to [this](http://www.deeplearningbook.org) book in the blog post. This is a summary of points I learnt from Chapter 6 which begins the Neural Networks Section from the Deep Learning book. This book is authored by Ian Goodfellow, Yoshua Bengio and Aaron Courville; an amazing resource to thoroughly understand the different concepts of Deep Learning. I already have a basic understanding of these models and I am reading this for gaining stronger theoretical depth.

### My Notes:

* Feedforward networks require us to choose the <strong>activation functions</strong> (sigmoidal, tan h etc) which are used to compute the hidden layer values, how many layers the network should contain, how many units each layer should contain, how these layers are connected to each other, the loss function and certain hyper-parameters for the back-propogation algorithm to function efficiently.

* Feedforward neural networks are typically represented by composing many different functions together. For eg, a 3 layer neural network can be represented by three functions f<sup>(1)</sup>,f<sup>(2)</sup> and f<sup>(3)</sup> connected in a chain to form f(x) = f<sup>(3)</sup>(f<sup>(2)</sup>(f<sup>(1)</sup>(x))  where each f represents a layer.

* The <strong>rectiﬁed linear activation unit</strong> yields a non linear transformation to the output of a linear transformation. However, since this function is a piecewise linear function with two linear pieces it remains very close to linear. They preserve many of the properties of linear models that make them easy to optimize with gradient-based methods and generalize well.
![Rectified Linear Activation Function]({{site.baseurl}}/images/relu.png)

* This nonlinearity of neural networks causes most loss function to become non-convex. This means that we must use <strong>stochastic gradient descent</strong> which does not guarantee convergence and is sensitive to the values of the initial parameters. It is therefore important to initialize all weights to small positive values.

* Cost Function choice: Most modern neural networks use the <strong>Cross Entropy function</strong> between the training data and model distribution (i.e. the negative log likelihood) described by: J(&Theta;) = -E<sub>x,y~p&#770;<sub>data</sub></sub> log P<sub>model</sub>(y/x)

* Choice of Cost Function is tightly coupled with type of Output Unit. Role of output layer is to produce some additional transformation on the features to result in the task that the network must perform. For <strong>Gaussian Output Distributions</strong>, we use linear units (i.e simple outputs based on affine transformations with no non-linearity. For <strong>Binary Output Distributions</strong>, we use Sigmoid Output Units . However Sigmoid saturates when the argument is very positive or very negative. i.e. function becomes insensitive to small changes in the input. Another function which can be used in its palce is the Softplus function. We can use Softmax units for <strong>Multinoulli Output Distributions</strong>.

![Output Units]({{site.baseurl}}/images/output_units.png)


