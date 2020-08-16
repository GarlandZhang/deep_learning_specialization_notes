- residual networks take advantage of skip connections to solve vanishing gradient problem ,tehrefore allowing to train deeper networks

## residual block
  - skip connection + "main path" which is the linear => relu, repeated, etc.
  
![res](https://i.gyazo.com/fb152f6c97c715091df0ca2ba460e54a.png)

## identity block

![id](https://i.gyazo.com/54e5a241111e71b57ca0cd15fa7662ed.png)

## benefit overview

![res](https://i.gyazo.com/68e53cf99114af731f15a7c12233a2a0.png)

## intuition
![eq](https://i.gyazo.com/da3050bb5c5ec11fc018c061a3675b37.png)
- with regularization, weights become smaller; suppose weights become so small that they are approx 0 and bias also happens to srhink to 0; then the intermediate layer contributes hardly anything!

- for skip connections to work, we need the dimensions to be the same (not problem if dimension is preserved); with pooling we need to reshape
