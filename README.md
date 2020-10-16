Inroduction
One major obstacle towards AI is the poor ability of models to solve new problems quicker, and without forgetting previously acquired knowledge. To better understand this issue, we study the problem of continual learning, where the model observes, once and one by one, examples concerning a sequence of tasks. First, we propose a set of metrics to evaluate models learning over a continuum of data. These metrics characterize models not only by their test accuracy, but also in terms of their ability to transfer knowledge across tasks. Second, we propose a model for continual learning, called Elastic Weights Consolidation (EWC) that alleviates forgetting, while allowing beneficial transfer of knowledge to previous tasks. Our experiments on variants of the MNIST , called Rotated MNIST.

Implement Elastic Weights Consolidation (EWC) Strategy
Introduction to the method:
Accroding to paper Overcoming catastrophic forgetting in neural networks, EWC can prevent catastrophic forgetting by constraining important parameters to stay close to their old values when performing new tasks.

While learning new task B, EWC therefore protects the performance in task A by constraining the parameters to stay in a region of low error for task A centered around the set of weights and biases  𝜃𝐴 

EWC also uses a posterior probability to justify this choice of constraint and decides which weights are most important for a task. In addition, it approximates the posterior as a Gaussian distribution with mean given by the parameters  𝜃𝐴  and a diagonal precision given by the diagonal of the Fisher information matrix F.

Here's the loss fucnction we're going to use in our project:

𝐿(𝜃)=𝐿𝐵(𝜃)+∑𝑁𝑖2𝜆𝐹𝑖(𝜃𝑖−𝜃∗𝑖,𝐴)2  Here, the  𝐿𝐵(𝜃)  is the loss function for new task only, the  𝜆  is the ewc lambda, which decides how important the previous task's parameters are to the new task, we also have  𝑖  labels each parameter.

When EWC moving with the third task or more task, it will try to keep the network parameters close to the learned parameters previous tasks since the sum of two quadratic penalties is itself a quadratic penalty.

Exploring on the EWC lambda:
Since the  𝜆  in our EWC loss function decides how important the previous task's parameters when compared to the new task, so we would want to find the best  𝜆  that fits our model which provides better accurracy:

In this part, we explores different  𝜆  values and run each of them for three tasks and then plot them together to find the best  𝜆  value for our model.

From the experiment, we can see the best  𝜆  value for our MNIST dataset is 0.35, which we used in our PART EWC training above for computing the loss fucntion.
