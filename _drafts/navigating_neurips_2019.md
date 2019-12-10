### Navigating NeurIPS 2019

It's a large conference with thousands of attendees from all over the world which is challenging enough for a person, 
and perhaps more so for an introvert who gets easily exhausted by social interaction or in crowds. I am still building
my working guide to navigating such spaces but I think some key steps that helped me are:

1. It's not always easy to find the time to prepare before hand, but if you are able to squeeze it in. This helps navigate it a 
1000x times better. 

2. Write down the key research interests you have and try to stick to delving deeper and broader into those. Trying to
explore everything is challenging, the over-stimulation is crazy and it needs to be filtered out and focused so you don't
drown yourself out.

3. Socialize and find your alone time in pockets.

4. Don't get burnt out.

5. How to critically analyze a paper.

### Poster sessions I attended:

#### Adversarial Learning

1. A Game Theoretic Approach to Class-wise Selective Rationalization 

Problem the paper tries to solve - One way to achieve interpretability in NLP is highlighting portions of text that 
influence the decisions of a neural network to produce a certain output. This is producing rationalizations for the output.
It can be done during training or post-hoc. Existing methods have some limitations such as lumping together information
that led the network to produce activations in different classes, together. 

Approach - CAR framework uses two factual rationale generators and two counterfactual rationale generators. These generate
rationales for labels other than the ground truth labels. There are two discriminators that discriminate between each pair of 
factual and counterfactual rationales. The setup allows for adversarial learning of the classification task.

Thoughts - Wonder if this approach is extendable to vision. Its a good idea for interpretability. The factual generator could
be trained to produce a mask over the input image for a class label l. The counter factual generator could be trained to produce
a mask over the input image for the class label l'. The input image is then masked with both of these and 
fed to the discriminator to classify it into the correct class. The mask can be controlled to upto 10% pixels in the image etc.
This provides easily interpretable classification systems.


2. A New Defense Against Adversarial Images: Turning a Weakness into a Strength

