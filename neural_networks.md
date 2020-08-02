logistic function aka **sigmoid activation function**

"Our input nodes (layer 1), also known as the "input layer", go into another node (layer 2), which finally outputs the hypothesis function, known as the "output layer".

We can have intermediate layers of nodes between the input and output layers called the "hidden layers."

In this example, we label these intermediate or "hidden" layer nodes "activation units."

example of a shallow neural network:

![nn](https://i.gyazo.com/6628a5ae7c1ae9e77c7bf7d2afc004f6.png)

**feed forward propagation** is the input feeding through the neural network from input to output. 

the activation function value for each layer node is calculated as follows:

![calc_node](https://i.gyazo.com/c9ddd49fb3b8776bdc4508cf2e85d581.png)

To compute the next layer, we must add a **bias node a0^(j) = 1** (always). 

note: since hypothesis output is just an activation node, then we just get a singular value. 

## applications

nn = functions, therefore we can create a shallow nn to replicate the OR gate function.

![OR](https://i.gyazo.com/2416fcff5bf881980857087ed159daf2.png)

more complex functions:

![XNOR](https://i.gyazo.com/0b9c7468119f0cd5a3bf339383e7bc13.png)

## multiclass classification

our final layer has n (= # classes) outputs where each output is the hypotheses output "guess" for that class. Using sigmoid activation function, each value will be approximately 0 or 1. 

take the max to get the guess. 
