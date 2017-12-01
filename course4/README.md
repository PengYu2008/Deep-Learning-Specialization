# Course4: Convolutional Neural Networks
The fourth course for [Deep Learning Specialization on Coursera](https://www.coursera.org/specializations/deep-learning).


## Objectives

1. To understand the convolution, pooling operation, and some terms: padding, stride, filter.
2. To know some classic networks, build DNN with [Keras](https://keras.io/).
3. Implement a Residual network.

## Assignments

* [week1](https://github.com/zyunsg/deep-learning/tree/master/course4/week1) 
* [week2](https://github.com/zyunsg/deep-learning/tree/master/course4/week2)

## Summary

1. **Convolutional Neural Networks: Step by Step**: to implement CONV and POOL layers... 
   * Convolution functions: transforms the input volume into an **different size** output volume
      - zero Padding: avoid shrinking height/width of the volumes. "same": height/width is exactly preserved after one layer
      - convolve window: apply filter by element-wise multiplying -> sum values up -> add bias
      - convolution forward
      - convolution backward
   * Pooling functions: help reduce height and width of the input, and make feature detectors more invariant to its position in the input
      - two types: Max-pooling, Average-pooling
      - no parameters to train, but have hyperparameters, such as window size f
      - pooling forward
      - pooling backward
   
2. **Convolutional Neural Networks: Application**: build ConvNet in TensorFlow for classification problem
   * model()
     * create placeholder() 
       - [tf.placeholder()](https://www.tensorflow.org/api_docs/python/tf/placeholder)
     * initialize parameters()
       - [tf.get_variable(, initializer=tf.contrib.layers.xavier_initializer(seed=0))](https://www.tensorflow.org/api_docs/python/tf/get_variable)
     * forward propagation(): Conv2D -> Relu -> Max pool -> Conv2D -> Relu -> Max pool -> Flatten -> Fullyconnected (FC) layer
       - [tf.nn.conv2d()](https://www.tensorflow.org/api_docs/python/tf/nn/conv2d)
       - [tf.nn.max_pool()](https://www.tensorflow.org/api_docs/python/tf/nn/max_pool)
       - [tf.nn.relu()](https://www.tensorflow.org/api_docs/python/tf/nn/relu)
       - [tf.contrib.layers.flatten()](https://www.tensorflow.org/api_docs/python/tf/contrib/layers/flatten)
       - [tf.contrib.layers.fully_connected()](https://www.tensorflow.org/api_docs/python/tf/contrib/layers/fully_connected)
     * compute cost()
       - [tf.nn.softmax_cross_entropy_with_logits()](https://www.tensorflow.org/api_docs/python/tf/nn/softmax_cross_entropy_with_logits)
       - [tf.reduce_mean()](https://www.tensorflow.org/api_docs/python/tf/reduce_mean)
     * optimizer()
       - [tf.train.AdamOptimizer().minimize(cost)](https://www.tensorflow.org/api_docs/python/tf/train/AdamOptimizer)
     * initialize all variables globally
       - [tf.global_variables_initializer()](https://www.tensorflow.org/api_docs/python/tf/global_variables_initializer)
     * start session: (loop for num_epochs, get and optimize each mini-batch)
     
3. **Keras tutorial - the happy house**: for rapid prototyping
   * four steps in Keras
      1. create the model 
         - define input placeholder: Input()
         - zero-padding: ZeroPadding2D()
         - CONV -> BN -> RELU block: CONV2D() -> BatchNormalization() -> Activation('relu')
         - Maxpool: MaxPooling2D()
         - flattn: Flatten()
         - fullyconnected: Dense()
         - create model: Model(inputs= , outputs= , name= )
      2. compile: model.compile(optimizer = "...", loss = "...", metrics = ["accuracy"])
      3. fit/train: model.fit(x = ..., y = ..., epochs = ..., batch_size = ...)
      4. evaluate/test: model.evaluate(x = ..., y = ...)
    * model.summary(): prints layers details
    * plot_model(): plot graph

4. **Residual Networks**: stacking blocks together, including identity and convolutional blocks
   * very deep "plain" networks don't work in practice because they are hard to train due to vanishing gradients
   * a shortcut or skip-connections help address the Vanishing Gradient probelm
   * two types of blocks
     - identity block: the dimensions of input and output are the same
     - convolutional block: the dimensions of input and output do not match up
     - the **main difference** between them is that there is a conv2d layer in the shortcut path.
   * implementation
     - [Conv2D](https://keras.io/layers/convolutional/#conv2d)
     - [BatchNorm](https://keras.io/layers/normalization/#batchnormalization)
     - activation: Activation('relu)
     - [Addition for shortcut path](https://keras.io/layers/merge/#add)
 
 ## References
 
 * **Residual Networks**
    - [Deep Residual Learning for Image Recognition (2015)](https://arxiv.org/abs/1512.03385)
    - [Francois Chollet's github repository](https://github.com/fchollet/deep-learning-models/blob/master/resnet50.py)



