normalize the neurons (Z values) by subtracting them by the mean and dividing by standard deviation:

![impl](https://i.gyazo.com/3c2c705c1864fe21c2aa1bb9bd881183.pngV)
  - gamma and beta are learnable parameters (this beta is not the same as that used in momentum or optimizer)
  - note: ![note](https://i.gyazo.com/8e2cbb535253a70313e5d5d3ab639129.png)
  
![nn](https://i.gyazo.com/af02c4faa36b07ce072da91dab6873b0.png)

## minibatches
  - because batch norm subtracts mean, and the bias is included in each of the Z values, then the bias is cancelled out
  
  ![min](https://i.gyazo.com/16b3eccae1a247f666f82a63618f2950.png)
  
## impl w/ grad desc
  - ![impl](https://i.gyazo.com/ad7f8a6cf14163902c8eb1920f7f0327.png)
  
