**Continual learning strategies(EWC) for rotated MNIST dataset**

**Group Members**

Ida Jebakirubai (is356@njit.edu),
Sudhan Rameshwaran  (sr64@njit.edu),
Yusuf Sabuwala (yes5@njit.edu)

**Description**

In this project we explored on Continual Learning technique using the rotated MNIST dataset in Colab notebook.

The approach we used is Elastic Weights Consolidation(EWC) which identifies the important features of the previous task and penalises the weights associated with them while training the new data. This enables the Neural Network to stay in a low error region for both the tasks.

![EWC overview](https://github.com/IdaStephen/DL-continual-Learning/blob/main/EWC%20overview.png)
![results comparison](https://github.com/IdaStephen/DL-continual-Learning/blob/main/results%20comparison.png)


**Dataset**
Training Dataset: 60000 * 28 * 28

Test Dataset: 10000 * 28 * 28

Rotation: Randomized rotation

![Dataset](https://github.com/IdaStephen/DL-continual-Learning/blob/main/Dataset.png)

**Project code**

Please use the below link to access the Colab notebook, the same has been attached in the GitHub repository.

https://colab.research.google.com/drive/1RLCVOYHjfd9wHhEX4LRk77i-5so__TMz?usp=sharing

**Result**

We were able to train 10 tasks using EWC with final accuracy of 85.78%:

![Result-EWC](https://github.com/IdaStephen/DL-continual-Learning/blob/main/Result_EWC.png)
