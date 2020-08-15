- generalized logistic regression
- outputs probabilities of each class (sums up to 1)

![nn](https://i.gyazo.com/571ebef20013f6c83dfb9d4a3febd17e.png)

e.g.; of how softmax is calculated:
![nn](https://i.gyazo.com/80729cec15d8e655fdadedfdb6442fd7.png)

## loss function
let C = 4
![lf](https://i.gyazo.com/62a65186fd91b715204cb15c37c1ea33.png)


## grad desc w/ softmax
- same as how we apply backprop to relu and sigmoid but now with softmax:

deriv:
![deriv](https://i.gyazo.com/869ab2e35655a8cf002a52129d4be61c.png)
