
This Problem consists of a Simple Neural Network that
  a.take 2 inputs:
    1. an image from MNIST data set, and
    2. a random number between 0 and 9
  b.and gives two outputs:
    1. the "number" that was represented by the MNIST image, and
    2. the "sum" of this number with the random number that was generated and sent as the input to the network
    
![image](https://user-images.githubusercontent.com/55537646/119216945-68ebc300-baf4-11eb-9869-61882d2f2350.png)


**Data Representation**
 
 According to problem statement,
 
 There are two types of Data Input
 
    1. Image
    2. Random Number 
    
 The output of the data will be
 
    1. Classification of Digit in the Image.
    2. Sum of The digit and random number.
 
For this Problem we are using MNIST data set. MNIST Handwritten Digit Classification Dataset. It is of 60,000 small square 28×28 pixel grayscale images of handwritten single digits between 0 and 9 for training and 10,000 data points for testing.

**torch.randint** will be used to create a 60000 Random Numbers to generate between 0 to 9


**Data generation strategy**

 "generate_data" is the function used that returns Image , Image Label ,random number , sum of label and random number which we can use to create a Data loader.
 
 "MNIST_Random_loader" method provides  required data for the model to Train and Test. We have Done one hot encoding to the random numbers and sum outputs in the loader function.
 
**Combination of two inputs**

Combination of two inputs done by

  1. Cascading model created for predicting MNIST that returns output of shape [1, 10]
  2. For this to happen we need to concatenate the Output on model 1 and input using torch.cat([mnist_d,Num],dim = -1)


**loss function**

MNIST CNN Model --  **Negative log likelihood loss**

Because It raise the confidence of correctly predicted class with huge margin.

**Epochs Image**

![image](https://user-images.githubusercontent.com/55537646/119234669-bb58ce00-bb4c-11eb-9812-1befaf981db3.png)
