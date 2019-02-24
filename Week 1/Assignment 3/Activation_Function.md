# Activation Functions

A neural network consists of multiple layers of neurons which can be activated for processing of input data. A mathematical model which decides which neuron would be activated to achieve the desired output is known as an activation function. <br/>

It is a non-linear transformation carried over the input data to extract the features having relevant information. <br/> <br/>

Mathematically, we define an activation function on a neuron Y as, <br/>

### Y = Function(summation(weight x input) + bias)<br/>

#### Importance of Activation Function:<br/>

If we do not use any activation function then the weights and bias of the data would do a simple linear transformation which cannot be applied to complex problems and essentially the entire neural network becomes a linear regression model which definitely cannot work on image processing or natural language processing. <br/>

### Commonly used Activation Functions:

<br/>
![Alt text]("https://github.com/vgaurav3011/EIP-3.0-/blob/master/Activation%20Function%20Diagrams/binary.png")



####  1. Binary Step Function:<br/>

It is commonly used for extremely simple classification problems where the answer can be a simple yes or no to a given problem. It indicates whether a neuron is active or not and if the value Y is above a given threshold value then activate the neuron otherwise no action is to be taken. <br/>

In simple maths, f(x) = 1 for x>=0<br/>

This may cause problems during back propagation because when the gradients are sent for computing errors then it does not handle them properly giving zero as output for most of them and thus improvement of models becomes restrained. <br/>

f'(x) = 0 for all values of x <br/>

### 2. Linear Function: 

<br/>

To overcome the problem of updating gradients during back propagation we make use of a simple step function to compute the errors of gradients. Mathematically, we can say that <br/>

f(x) = ax and thus f'(x) = a<br/>

Now, everytime we perform a back propagation the gradient would remain same and this becomes a problem as the model really does not improve as expected.

### 3. Sigmoid Function:

<br/>

It is a widely used activation function especially in cases of determining of the probability since it has a range of [0,1]. Mathematically, <br/>

f(x) = 1/(1+e^-x)<br/>

A smooth function having continual differentiability and can handle non-linear variations of data. Thus, it generates non-linear outputs as well. The gradient is extremely high between the values of 3 and -3 but gets much flatter in other regions. Therefore, it is desirable to use for classification based problems. However, the sigmoid function cannot handle negative range of values. <br/>

### 4. Tan h Function:

<br/>

A scalable version of the sigmoid function which can handle negative values too. <br/>

Mathematically, <br/>

tanh(x) = 2.sigmoid(2*x) <br/>

The gradient of the tan h function is steeper as compared to the sigmoid function. This choice of using the sigmoid function or the tan h function depends upon the requirement of the gradient problem statement. However, similar to the sigmoid function the vanishing gradient problem still remains an issue here as well. <br/>

### 5. Rectified Linear Unit (ReLU) Function: 

<br/>

A non-linear function defined as f(x) = max (0, x)<br/>

It can easily perform backpropagation as it is non-linear and have multiple layers of neurons being activated by a single function. Its essence lies in the fact that it does not activate all the neurons at the same time. If the input is negative then it will convert it to zero and the neuron does not get activated creating a sparse network which is efficient and easy to compute. <br/>

The ReLU function also has issue of gradients approaching towards zero and thus some weights never get updated during back propagation which leads to dead neurons. <br/>

### 6. Leaky Rectified Linear Unit Function: 

<br/>

Leaky ReLU function is an improved version of ReLU function. It handles some values below the range of zero too. Mathematically, <br/>

f(x) = ax for x<0, x=0 and x>0 too <br/>

The main advantage of replacing the horizontal line is to remove the zero gradient.So, in this case the gradient of the left side of the graph is non zero and so we would no longer encounter dead neurons in that region.  <br/>

### 7. Softmax Function: 

<br/>

A suitable function to handle classification problems and has an advantage over sigmoid function as it is applicable to multiple classes. It determines the outputs for each class between 0 and 1 and would also divide by the sum of the outputs. This essentially gives the probability of the input being in a particular class. It can be defined as: <br/>

Mathematically, we have: <br/>

### 8. Scalable Exponential Linear Unit Function(SeLU):

Essentially a ReLU function but can handle negative output values and also has ability to predict the values better. It has a gradual smooth curve compared to ReLU.<br/>







  
