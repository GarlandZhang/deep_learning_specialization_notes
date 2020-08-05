
choose some points in dataset as **landmarks**

![kernel](https://i.gyazo.com/e4cf9279bc9f5246ddb4bcc26a370f3f.png)
  - kernel fn is the similarity fn
  - "x values close to landmarks are "similar" and therefore are approx 1

![ex](https://i.gyazo.com/f03dc47f7f2cbf989c98ece0b0b54599.png)

how do kernels in SVMs help create decision boundaries:
![kern](https://i.gyazo.com/ad69fb89b0bf76b01a43bb89f2fae149.png)
  - substitute x1, x2, etc.. with f1, f2, etc..
  - suppose we train to find the corresponding thetas
  - then based on the data points relative to the landmarks, we can plug into our hypothesis and determin if >= 0
  - if >= 0, predict y =1, otherwise predict y= 0
  - we therefore get a decision boundary

## choosing landmarks

![choose](https://i.gyazo.com/6e29224bd9d28bc5b1e03fec1108bbf0.png)

