# Week2 Quiz: Autonomous driving (case study)

1. To help you practice strategies for machine learning, in this week we’ll present another scenario and ask how you would act. We think this “simulator” of working in a machine learning project will give a task of what leading a machine learning project could be like!

    You are employed by a startup building self-driving cars. You are in charge of detecting road signs (stop sign, pedestrian crossing sign, construction ahead sign) and traffic signals (red and green lights) in images. The goal is to recognize which of these objects appear in each image. As an example, the above image contains a pedestrian crossing sign and red traffic lights
    <br/><img src="./images/q1.PNG"><br/>
    Your 100,000 labeled images are taken using the front-facing camera of your car. This is also the distribution of data you care most about doing well on. You think you might be able to get a much larger dataset off the internet, that could be helpful for training even if the distribution of internet data is not the same.

    You are just getting started on this project. What is the first thing you do? Assume each of the steps below would take about an equal amount of time (a few days).
    - [ ] Spend a few days collecting more data using the front-facing camera of your car, to better understand how much data per unit time you can collect.
    - [ ] Spend a few days getting the internet data, so that you understand better what data is available.
    - [ ] Spend a few days training a basic model and see what mistakes it makes.
    - [ ] Spend a few days checking what is human-level performance for these tasks so that you can get an accurate estimate of Bayes error.
 
2. Your goal is to detect road signs (stop sign, pedestrian crossing sign, construction ahead sign) and traffic signals (red and green lights) in images. The goal is to recognize which of these objects appear in each image. You plan to use a deep neural network with ReLU units in the hidden layers.

   For the output layer, a softmax activation would be a good choice for the output layer because this is a multi-task learning problem. True/False?
    - [ ] True
    - [ ] False

3. You are carrying out error analysis and counting up what errors the algorithm makes. Which of these datasets do you think you should manually go through and carefully examine, one image at a time?
    - [ ] 10,000 images on which the algorithm made a mistake
    - [ ] 10,000 randomly chosen images
    - [ ] 500 images on which the algorithm made a mistake
    - [ ] 500 randomly chosen images

4. After working on the data for several weeks, your team ends up with the following data:
   + 100,000 labeled images taken using the front-facing camera of your car.
   + 900,000 labeled images of roads downloaded from the internet.
   + Each image’s labels precisely indicate the presence of any specific road signs and traffic signals or combinations of them. For example. y^(i) = [1 0 0 1 0] means the image contains a stop sign and a red traffic light.
   Because this is a multi-task learning problem, you need to have all your y(i) vectors fully labeled. If one example is equal to [0 ? 1 1 ?] then  the learning algorithm will not be able to use that example. True/False?
   - [ ] True
   - [ ] False

5. The distribution of data you care about contains images from your car’s front-facing camera; which comes from a different distribution than the images you were able to find and download off the internet. How should you split the dataset into train/dev/test sets?
   - [ ] Choose the training set to be the 900,000 images from the internet along with 80,000 images from your car’s front-facing camera. The 20,000 remaining images will be split equally in dev and test sets.
   - [ ] Choose the training set to be the 900,000 images from the internet along with 20,000 images from your car’s front-facing camera. The 80,000 remaining images will be split equally in dev and test sets.
   - [ ] Mix all the 100,000 images with the 900,000 images you found online. Shuffle everything. Split the 1,000,000 images dataset into 600,000 for the training set, 200,000 for the dev set and 200,000 for the test set.
   - [ ] Mix all the 100,000 images with the 900,000 images you found online. Shuffle everything. Split the 1,000,000 images dataset into 980,000 for the training set, 10,000 for the dev set and 10,000 for the test set.
   
6. Assume you’ve finally chosen the following split between of the data:

            | Dataset:        | Contains: | Error of the algorithm: |
            |  Training       | 940,000 images randomly picked from (900,000 internet images | 3MB         |
                                + 60,000 car’s front-facing camera images)  
            
            |  Training-Dev   | 1 sec   | 3MB         |
            |  Dev            | 1 sec   | 3MB         |
            |  Test           | 1 sec   | 3MB         |  
