                                                                              BACKGROUND AND VERY BASICS
                                                                              
Please refer below question and answers on which i tried to explain terminolgies in lay man terms

1.  What is a neural network neuron?

      •	In General, Neuron is an entity that has ability to store, transfer, transform, and process/compute (applicable only to neurons in human brain) information.

      •	Unlike neurons in human brain, Neural Network neurons acts just a storage container that stores data at instant of time.

      •	Each neuron in neural network has ability to receive inputs, store data and transfers it to other neurons.

      •	Each layer in neural network has fixed number of neurons. Please refer the simple neural network image below on which the first layer has 3 neurons and it is also called           Input Layer and last layer has single neuron which is also called Output Layer.

      ![image](https://user-images.githubusercontent.com/55537646/117194714-0b702a80-ae02-11eb-8941-e69af03ed1e9.png)

      •	Each neuron in one layer is connected to every neuron in other layer as shown in the image.

2. What is the use of the learning rate?

    •	When we deal with neural networks our major motive is to produce the output that minimizes loss.
    •	It requires updating weights by taking partial derivate of loss with respect to appropriate weight.
                                 ![image](https://user-images.githubusercontent.com/55537646/117194832-2fcc0700-ae02-11eb-9fa0-f378fa03b8f3.png)
         
    •	Because we must change the weight (derivative) in such a way that derivate of other weights are negligible.
    •	To ensure this the parameter **learning rate(alpha)** is introduced, hence change in one weight (very small) will not affect other weights (as all the parameters are dependent       on each other) that indeed affects the whole function.

**Case 1: Smaller Learning Rate**
    •	If the Learning rate is too small our result will be accurate as it will keep an eye on more decimal places in weights but our training time would be very high, as it will       take more time to converge the loss function with minuscule change in weights.
    
![image](https://user-images.githubusercontent.com/55537646/117195518-fba51600-ae02-11eb-8f5b-f6fb64fe887e.png)


**Case 2:  Larger Learning Rate**
    •	Larger learning rate makes the convergence uncertain, sometimes it minimizes sometimes it maximizes which makes divergence of our loss.
    
![image](https://user-images.githubusercontent.com/55537646/117195500-f6e06200-ae02-11eb-8cc4-efde6221df87.png)


Learning rate should always be optimal that literally makes loss to converge gradually to attain minima.

![image](https://user-images.githubusercontent.com/55537646/117195337-ca2c4a80-ae02-11eb-96b4-7b40862f9764.png)


3.	How are weights initialized?

      Weights needs to be initialized by considering below points:
      
        •	Weights should be small (not too small as it creates vanishing gradient problem).
        
        •	Weights should not be same or zero for obvious reasons as the behaviour will be same.
        
        •	Weights should have good variance.
        
    Below are the techniques followed for weights initialization.
      
    •	**Uniform initialization** – weights follow uniform distribution between in the range (-1/no of input neuron, 1/no of input neuron) – works well with sigmoid                     activation function
        
    •	**Xavier / Gorat**  – works well with sigmoid activation function
        
      •	**Xavior Normal**  – follows normal distribution between 0 and standard deviation
      
      •	**Xavior Uniform** – uniform distribution between certain range of values (has some formula)
            
    •	**He initialization** - works well with relu activation function
        
      • **He Uniform**
      •	**He Normal**
            
      Below excel function initializes weights for beginers to practice in Excel 
      
      **NORM.INV(RAND(),0,1)**
      
4.	**What is "loss" in a neural network?**
     
     Loss is the measure of how the predicted output varies with the ground truth.
     
     Neural networks accuracy would be determined based on its efficiency to minimize the loss. 

     To identify Loss one can makes use of relevant loss functions.

     Most common loss functions are
       
        1.Mean Square Loss
        2.Cross Entropy Loss
        3.Maximum Likelihood Loss

     Loss function plays a major role during back propagation in terms calculating gradients.

5. What is the "chain rule" in gradient flow?
