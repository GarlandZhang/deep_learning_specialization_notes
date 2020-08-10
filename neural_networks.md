e.g.;
![ex](https://i.gyazo.com/d538c171e872935d191677610b12a947.png)


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

our final layer has n (= # classes) outputs where each output is the hypotheses output "guess" for that class. Using sigmoid activation function, each value will be approximately 0 or 1. The output vector will ideally look like a **one-hot vector**

take the max to get the guess. 


## cost function

**assumption**: nn is for classification

cost function is simply the logistic regression for each of the K class outputs. with regularization, we use every weight in the neural network. 

![mm_cf](https://i.gyazo.com/a91945958fc9168df3f1ed831848a278.png)

## backpropagation algorithm

""Backpropagation" is neural-network terminology for minimizing our cost function, just like what we were doing with gradient descent in logistic and linear regression"

to calculate the partial derivative of each wewight:

![backprop](https://i.gyazo.com/af7f4504c2751f9dd9685f1ba52d203f.png)

the triangles are the gradients (unnormalized). the D values are the gradients.

to calculate the partial derivatives, we perform forward propagation first. we then need to solve for the 8s (= error between actual to guess values). then we calculate the unnormalized gradient and accumulate to our triangles. finally, we normalize the values.

note: to calculate the 8s, we go from right to left (hence, backpropagation).

## implementation specific
in order to levarage optimizing functions like fminunc, we need to convert matrices into vectors (aka **unrolling parameters**).

![adv_op](https://i.gyazo.com/24acd636e3093577808f4f0c15365afa.png)

## gradient checking

ensures backpropagation is implemented properly and works as intended.

approximate derivatves by taking a small epsilon, E, and compute J(0 + E) - J(0 - E) / 2. With partial derivatives, we use the same formula but fix all 0s except the relevant 0. 

![gc](https://i.gyazo.com/aff33fb9a5b4659b500730fa9462d4e5.png)

this is computationally expensive so do it once and turn it off for normal training

## random initialization

do not set all weights to 0 initially (no improvement when training!). instead, use unifrom distribution to randomly init weights.

![ri](https://i.gyazo.com/d411017feaf597b2ea090fe15a6c271d.png)


## neural network summary

![summary](https://i.gyazo.com/e6691ee2463a7120683458b00df134d7.png)
