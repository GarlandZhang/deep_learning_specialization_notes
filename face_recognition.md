## face verification vs face recognition

![verif](https://i.gyazo.com/8f9a0d3faa65cbea40dabf2f51c8ad71.png)
  - recognition relies on a very accurate verification model
  
## one shot learning
  - can only look at a new image once and needs to verify
  
![similarity](https://i.gyazo.com/2790af49a63c020270de495ebcea7336.png)
  - we choose the face with the lowest degree of difference
  - if theres a face where the lowest degree is > some threshold, then that face does not belong in the dataset
  
## siamese network
  - encode images and measure distance to determine degree of difference
![siamese](https://i.gyazo.com/70101841ca59b9563d2012e6992793f9.png)

## triplet loss
  - always looking at 3 images while training: anchor, positive (same person as anchor), and negative (not same person as anchor)
 ![anc](https://i.gyazo.com/fce2e15943661e409dcadd78530ae6f8.png)
  - we want the distance of the encodings between A, P to be super small compared to A, N (not just smaller, MUCH smaller). This is why we have **alpha** which is the margin
 ![learning_obj](https://i.gyazo.com/2773a95788380de7f09ed2c32c6dcb86.png)
 
### loss fn
 ![loss](https://i.gyazo.com/29e52cd9895823b59d8f08abf27c3806.png)
  - we cannot have negative loss so we have a max of 0
  
### choosing triples A, P, N
  - its easy to satisfy the above constraint by randomly choosing images, but if we we choose images where d(A, P) is approx equal to d(A, N) then this is much harder:
![triplets](https://i.gyazo.com/86dfd7c1c9d6e21537fa63bddf23e1e8.png)

## face verification and binary classification
  - siamese network can combine the 2 encodings into 1 output w/ sigmoid:
![learn](https://i.gyazo.com/d1ef92750cb3dcceeeb16c84399fe14e.pngV)
  - the absolute difference is one way we can combine the 2 encodings together into 1 output
  - we can precompute encodings to prevent running through the neural network over and over again
  
  
