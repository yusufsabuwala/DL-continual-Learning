**Continual learning strategies(EWC) for rotated MNIST dataset**

**Group Members**

Ida Jebakirubai (is356@njit.edu),
Sudhan Rameshwaran  (sr64@njit.edu),
Yusuf Sabuwala (yes5@njit.edu)

**Description**

In this project we explored on Continual Learning technique using the rotated Mnist dataset in Collab notebook.
The strategy we used is Elastic Weights Consolidation(EWC) which avoids the catastrophic forgetting in neural network by constraining important parameters to stay close to their old values when performing new tasks.

**Dataset**
Training Dataset: 60000 * 28 * 28

Test Dataset: 10000 * 28 * 28

Rotation: Randomized rotation

![Dataset](https://github.com/IdaStephen/DL-continual-Learning/blob/main/Dataset.png)

**Project code**

Please use the below link to access the collab notebook, the same has been attached in the github repository.

https://colab.research.google.com/drive/1RLCVOYHjfd9wHhEX4LRk77i-5so__TMz?usp=sharing

**Result**

We were able to train 10 tasks using EWC with final acc 85.78%:

![Result-EWC](https://github.com/IdaStephen/DL-continual-Learning/blob/main/Result_EWC.png)
