normalize the neurons (Z values) by subtracting them by the mean and dividing by standard deviation:

![impl](https://i.gyazo.com/3c2c705c1864fe21c2aa1bb9bd881183.pngV)
  - gamma and beta are learnable parameters (this beta is not the same as that used in momentum or optimizer)
  - note: ![note](https://i.gyazo.com/8e2cbb535253a70313e5d5d3ab639129.png)
  
![nn](https://i.gyazo.com/af02c4faa36b07ce072da91dab6873b0.png)

## minibatches
  - because batch norm subtracts mean, and the bias is included in each of the Z values, then the bias is cancelled out
  - mean and dev are from the minibatch (and not the entire batch)
  ![min](https://i.gyazo.com/16b3eccae1a247f666f82a63618f2950.png)
  
## impl w/ grad desc
  - ![impl](https://i.gyazo.com/ad7f8a6cf14163902c8eb1920f7f0327.png)
  
## learning on shifting input distribution
  - e.g.; trained classifier on black cats => using on coloured cats; does not work well because domain changed
  - called covariate shift
![cov_shift](https://i.gyazo.com/64915e6288b71d293007131b3cc71c35.png)
  - with batch norm, we reduce the distribution of the input values (because mean and variance will be approx same) so the later layers will be stable and not "frfeak out" with these coloured cat images as distribution is approx same!

![nn](https://i.gyazo.com/b175e8e730889967e90feba9ed92a71f.png)
  
## batch norm as regularization
  - has a slight regularization effect by adding "noise" (aka normalizing the z values) in the hidden layer values; similar to how dropout adds "noise" by scaling values and eliminating values 
  - not reommended to use as regularization though
  
## batch norm at test time
  - during training time we use batch norm for a minibatch 
  - during test time, we might only get one input at a time sowe create mean and dev using exponentially weighted average
  
