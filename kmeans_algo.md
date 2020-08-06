
most widely used clustering algorithm

1. randomly create K points (called **cluster centroids**) 
2. color all data points the same color as the closest centroid
3. update the centroids to each be the average point amongst its brethen
4. continue doing this for however many times

![graph](https://i.gyazo.com/8f6e97ce8196ba1d4ac5d74e2ef9b1bb.png)

![algo](https://i.gyazo.com/36d371af47ddec13c10632123415d214.png)

## non separated clusters

![non-sep](https://i.gyazo.com/085cd6aea015116bd773cf18aaeace0d.png)

## optimization objective

![optim_obj](https://i.gyazo.com/ef08a86ff90dc1f9e1a5ed2d68135f42.png)

in the algo:

![algo](https://i.gyazo.com/36d371af47ddec13c10632123415d214.png)
  - observe in the first for loop we optimize w.r.t c(i), thereby minimizing sum of distance between centroids
  - in the second for loop, we optimize the centroids themselves, thereby minimizing sum of distance between paired points
  
## random initialization

- set the centroids to be randomly chosen training examples!

### local optima

![local_optima](https://i.gyazo.com/1e4a8c3be33c450b0dd127145de07d85.png)
  -  **sollution**: do multiple random intiializations and choose one with lowest cost
  
## number of clusters
- usually choose by hand

### elbow method
![elbow](https://i.gyazo.com/387120495b354bf7c25b88d6f6a0e651.png)
- choose # of clusters at "elbow"
- not used often if not obvious what "elbow" actually is (2nd graph)

### depends on use case (e.g.; tshirt sizes)
![value_of_k](https://i.gyazo.com/29d8e998f855c9952c27ca00c54e8f33.png)


