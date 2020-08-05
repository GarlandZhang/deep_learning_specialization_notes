a supervised learning algorithm

## logistic regression vs SVM

![log](https://i.gyazo.com/25895625df381983386e7befbca61d11.png)

![SVM](https://i.gyazo.com/6df78e650d3286de57f69b617179b93a.png)
  - derived from logistic regression with slightly different format (the theta solution is just a linear equation difference of the theta for logistic regression)
  - C = 1 / lambda
  - cost fn is sigmoid
  
SVMs are also called **large margin classifiers**:
  - logistic reg
  ![log](https://i.gyazo.com/ac10ce747eabe6ca34815d6d78f749e0.png)
  
  - SVM (so we require the theta'X to be much larger in magnitude, hence the large margin
  ![SVM](https://i.gyazo.com/8bfb3fc98e5b5b7008eae84a61d5f029.png)
  
### SVM decision boundary
why are SVMs superior to logistic regression? Not only does it do what logistic regression does (find a boundary to split the positive and negative examples), it finds the **most optimal** boundary

![ex](https://i.gyazo.com/0932c33c80008a96a97f75fa2f01af51.png)
  - this is possible because when the magnitude of the cost is >= 1, we approx get 0 and all thats left is the regularization term, so we optimize for the thetas to be as small as possible:
  ![reg](https://i.gyazo.com/a69eccbd6b917dd9b495db08237c1dbe.png)
  
  - in summary:
  ![cfn](https://i.gyazo.com/258d5a97eade3e4de0cb058e373be934.png)
  
### outliers
- recall that C = 1 /lambda and acts inversely to lambda
- therefore if C is large, then lambda is small, so the model will overfit the training data
- but if C is not too large, then lambda is not small, so the model will not overfit the training data

![lmi](https://i.gyazo.com/976feedee58a5ed23ea95641496dfa48.png)


## kernels
see: https://github.com/GarlandZhang/ml_notes/edit/master/kernels.md


## applying kernels to SVMs

![ker](https://i.gyazo.com/2323d41c446311225f70c8f6126578f8.png)
  - observe the slight modification made to regularization term: we iterate over the # of training examples as we have equal # of thetas as training examples + 1
  - why do we have m + 1 thetas? because we need m + 1 features, where we create a feature for each training example; we also have theta0.
  
## parameters summary

![param](https://i.gyazo.com/a846c7761913ad2fe852601c0272f465.png)

## in practice
**do not write your own software to determine theta parameters; much more optimized algos to solve**

![ssummary](https://i.gyazo.com/04e758f693fef78aadb6751dc5d90896.png)
  -note: perform feature scaling before using gaussian kernel to ensure f doesn't blow up when calculating euclidean distance in gaussian kernel

## svm, logistic regression, or NN?

![choices](https://i.gyazo.com/d94f633b573b99778a984c527af3ef86.png)

