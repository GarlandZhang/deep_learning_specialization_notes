- when you dont know what filter size to use, try them all! this is what inception network does:

![inc](https://i.gyazo.com/31e1c6dc4cf2049fe7f10228d9ad1cbe.png)

problem: computational cost

![comp](https://i.gyazo.com/d413e8ad93e1b5f37b004b55fdbce915.png)

solution: use 1x1 convolution!

![cost](https://i.gyazo.com/9df7c1e3e093212754b38d95b15a919a.png)
  - bottleneck layer is created to get same result 
  
## overview

![over](https://i.gyazo.com/98e57fe1c220b918ca0e09dafc0d9b0d.png)
  - with pooling, instead of 1x1 conv beforehand, we apply it after to reduce # of filters since pooling (when keeping 'same') will not change # of filters
  
![over](https://i.gyazo.com/eb1b67acf9f48da65eedfa7b7ad4b4e0.png)

