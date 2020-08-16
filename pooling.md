## max pooling

![max](https://i.gyazo.com/0e08133e382bebf8fc6b12f33d8e85ee.png)
  - note: no parameters to learn (has hyperparameters but gradient descent does not learn anything here)
  
## avg pooling

![avg](https://i.gyazo.com/f962267de01f8f92542fa8620598e3d8.png)
  - also no parameters to learn
 
- note: pooling still affects gradient descent but not directly; in backprop, we create a mask which tells us which values contributed to the pooling value (e.g.; if its max, then a matrix of equal shape will be all 0 except the location of max value which will be 1). The value we calculate is dZ. With avg pooling, we have a matrix where each element is 1 / # values in filter. 

![ex](https://i.gyazo.com/272227497502806c7719d3dcb3dcd903.png)
