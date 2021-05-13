**Neural Network from Scratch using Excel**

**Screenshot of values during forward and backward pass
**

![image](https://user-images.githubusercontent.com/55537646/118095617-ec6b2d00-b3ed-11eb-9427-de89f8da7765.png)

**Steps**

1.	Create a sample neural network with two neurons in hidden and output layer for reference as shown below.

![image](https://user-images.githubusercontent.com/55537646/118094834-e3c62700-b3ec-11eb-8f6a-7887031a84e6.png)

Where
i1, i2 – inputs.
h1, h2 – Neurons in hidden layer.
a_h1, a_h2 – outputs of h1 and h2 activated using sigmoid activation function.
o1, o2 – Neurons in output layer.
a_o1, a_o2 -- outputs of o1 and o2 activated using sigmoid activation function.
E1, E2 – Errors from two output units (Calculated using L2 Loss function)
W1 to w8 – weights.
E_Total – Total Error.


2.	Initialize inputs, weights, and targets (to calculate Loss from generated output).
3.	Calculate h1,h2,a_h1,a_h2,o1,o2,a_o1,a_o2,E1,E2, E_total, and learning rate for forward pass by substituting the below formulas.

h1 = w1*i1 + w2*i2
h2 = w3*i1 + w4*i2
a_h1 = 𝛔(h1) = 1/(1+exp(-h1))
a_h2 = 𝛔(h2) = = 1/(1+exp(-h2))
o1 = w5*a_h1 + w6*a_h2
o2 = w7*a_h1 + w8*a_h2
a_o1 = 𝛔(o1)
a_o2 = 𝛔(o2)
E1 = ½*(t1 - a_o1)²
E1 = ½*(t2 - a_o2)²
E_total = E1 + E2

4.	Calculate partial derivatives for all the functions with respect to each weight, while calculation derivative of activation function which is not elaborately mentioned in excel is below.
Sigmoid 

        = g(x) 
        
        = 1/1+e-x 
 
        = (1+e-x)-1

Derivative of sigmoid = g’(x) = (-1)  *  (1+e-x)-2   * (-e-x)
			
                      = (e-x/(1+e-x))* (1/(1+e-x))
               
                      = (1-1+e-x/(1+e-x))* g(x)
  
                      = g(x)*(1 – g(x))
                      
5.	Substitute the respective values in the resultant equations of backward pass and calculate new weights by subtracting original weight with learning rate times the updated weight.
6.	Update the new weights and repeat the same process for certain number of epochs.
7.	Reduction in total loss on each iteration could be witnessed in graph as below

![image](https://user-images.githubusercontent.com/55537646/118095175-60f19c00-b3ed-11eb-8a36-d453f5417a21.png)

Below are the Graph plots for error functions with different learning rates, It is evident that loss converges fast to global minima if we increase the learning rate.

Learning Rate = 0.1

![image](https://user-images.githubusercontent.com/55537646/118095265-7a92e380-b3ed-11eb-968e-35cdcb564b32.png)

Learning Rate = 0.2

![image](https://user-images.githubusercontent.com/55537646/118095289-81b9f180-b3ed-11eb-9e3e-da9be786271d.png)
 
Learning Rate = 0.5

![image](https://user-images.githubusercontent.com/55537646/118095303-85e60f00-b3ed-11eb-8d6c-ca37272aaa1a.png)
 
Learning Rate = 0.8

![image](https://user-images.githubusercontent.com/55537646/118095320-8bdbf000-b3ed-11eb-94ae-39c5572da02f.png)
 
Learning Rate = 1

![image](https://user-images.githubusercontent.com/55537646/118095330-90080d80-b3ed-11eb-867a-74de9e22f8cf.png)

Learning Rate = 2

![image](https://user-images.githubusercontent.com/55537646/118095336-94342b00-b3ed-11eb-93ff-445f679d17c4.png)

 






