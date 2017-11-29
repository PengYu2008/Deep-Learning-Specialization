# Course2: Improving Deep Neural Networks: Hyperparameter tuning, Regularization and Optimization
The second course for [Deep Learning Specialization on Coursera](https://www.coursera.org/specializations/deep-learning).


## Objectives & Conclusions:
* [week1](https://github.com/zyunsg/deep-learning/tree/master/course2/week1): Implement different types of **initialization**, L2 and dropout **regularization**, **Batch normalization** and **gradient checking**, check their corresponding performance.
  * Initialization: a well initialization can speed up the convrgence of gradient descent and increase the odds of gradient descent converging to a lower training error.
     - Different initializations lead to different results (Zero/Random/He initialization)
     - The weights should be initialized randomly to break symmetry, while the biases can be initialized to zeros. Random initialization is used to break symmetry and make sure different hidden units can learn different things.
     - Don't intialize to values that are too large
     - He initialization works well for networks with ReLU activations. 
  * Regularization: reduce overfitting.
     - Regularization will drive weights to lower values.
     - L2 regularization and Dropout are two very effective regularization techniques.
     - L2 regularization: the term is added to the cost, extra term in backpropagation, weight decay.
     - Dropout: use only during training, not during test time; apply both during forward and backward propagation; scale neurons value (by dividing keep_prob)
  
  * Gradient Checking
* [week2](https://github.com/zyunsg/deep-learning/tree/master/course2/week2): Implement and apply a variety of optimization algorithms, **Stochastic Gradient Descent(SGD)**, **mini-batch gradient descent**, **Momentum**, **Adam**, and check for their convergence. 
  * Optimization
* [week3](https://github.com/zyunsg/deep-learning/tree/master/course2/week3): Implement a neural network in **TensorFlow**. 
  * Tensorflow
 


