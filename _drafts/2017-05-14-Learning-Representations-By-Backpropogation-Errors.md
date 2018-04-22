---
layout: post
title: Why do we need Biases or Activation Functions?
category: posts
---

<h2>Question 1: Why do we need Biases?</h2>

Let us suppose that we have 1 input and 1 output. The output of the node j is calculated by multiplying the input from node i with 
the weight of the branch w<sub>0</sub>. Then we take the sigmoid (the activation function) of this output through the sigmoid function: 1/(1+e<sup>-x</sup>)

The graph below shows the various functions based on different values of the weight w(j,i).

![Sigmoid Function With Different Weights]({{site.baseurl}}/images/sigmoid_function.png) 

We can see that changing the weight of the branch only changes the "steepness" of the sigmoid. However, what if you wanted to shift the entire curve
by a constant amount to the right or the left?

To do that, you need a bias.

A bias value can be visualized as another input to the node j with a weight associated w<sub>1</sub>. The value of the bias is 1.0 so the output of the network now becomes: <math>sigmoid(w<sub>0</sub>*x<sub>0</sub>+w<sub>1</sub>*1.0)</math>.

![Sigmoid Function With Different Bias]({{site.baseurl}}/images/bias.png) 

Now as you can see, we can move the output around on the x-axis through the bias.

<h2>Question 2: Why do we need Activation Functions?</h2>

<p> If a node does not have an activation function, it is equivalent to having a linear activation function of <math>x*1</math>. 
Having a non linear activation function allows the outputs to learn more complex functions than linear regression. It also restricts the range of the output between two values. Linear activation functions like <math>f(x)=7.6*x+0.9*y</math> does not work since the output learned function from this equation would still be linear. The weight multiplication at each layer is just a linear transformation while the bias vector addition is only an affine transformation. All of these functions can be condensed into a single transformation. </p>




