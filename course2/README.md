# Course2: Improving Deep Neural Networks: Hyperparameter tuning, Regularization and Optimization
The second course for [Deep Learning Specialization on Coursera](https://www.coursera.org/specializations/deep-learning).

## Objectives: 
- Implement different types of **initialization**, L2 and dropout **regularization**, **Batch normalization** and **gradient checking**, check their corresponding performance.
- Implement and apply a variety of optimization algorithms, **Stochastic Gradient Descent(SGD)**, **mini-batch gradient descent**, **Momentum**, **Adam**, and check for their convergence. 
- Implement a neural network in **TensorFlow**. 

## Assignments & Conclusions:
* [week1](https://github.com/zyunsg/deep-learning/tree/master/course2/week1)
  * Initialization
     - Different initializations lead to different results(Zero/Random/He initialization)
     - The weights $W^{[l]}$ should be initialized randomly to break symmetry, while the biases $b^{[l]}$ can be initialized to zeros. Random initialization is used to break symmetry and make sure different hidden units can learn different things.
     - Don't intialize to values that are too large
     - He initialization works well for networks with ReLU activations. 
  * Regularization
  * Gradient Checking
* [week2](https://github.com/zyunsg/deep-learning/tree/master/course2/week2)
  * Optimization
* [week3](https://github.com/zyunsg/deep-learning/tree/master/course2/week3)
  * Tensorflow
 


