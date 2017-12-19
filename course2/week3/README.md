# Week3 Quiz: Hyperparameter tuning, Batch Normalization, Programming Frameworks

1. If searching among a large number of hyperparameters, you should try values in a grid rather than random values, so that you can carry out the search more systematically and not rely on chance. True or False?
   - [x] True
   - [ ] False

2. Every hyperparameter, if set poorly, can have a huge negative impact on training, and so all hyperparameters are about equally important to tune well. True or False?
   - [ ] True
   - [x] False

3. During hyperparameter search, whether you try to babysit one model (“Panda” strategy) or train a lot of models in parallel (“Caviar”) is largely determined by:
   - [ ] Whether you use batch or mini-batch optimization
   - [ ] The presence of local minima (and saddle points) in your neural network
   - [ ] The amount of computational power you can access
   - [x] The number of hyperparameters you have to tune

4. If you think β (hyperparameter for momentum) is between on 0.9 and 0.99, which of the following is the recommended way to sample a value for beta?
   - [ ] 
'''python
r = np.random.rand()
beta = r*0.09 + 0.9 
'''
   - [ ]
   - [ ]
   - [ ]
