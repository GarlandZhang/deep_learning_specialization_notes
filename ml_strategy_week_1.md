
## Orthogonalization

### tv tuning example

each knob on an old school tv has a separate purpose. One is to tune rotation, another for translation, etc. Therefore much easier to tune to ideal image.



### chain of assumptions in ML

1. Fit training set well on cost function
  - bigger network
  - change optimization algorithm
  
2. Fit validation set well on cost function
  - Regularization
  - Bigger training set (overfit on current training set)
3. Fit test set well on cost function
  - Bigger validation set (overfit on current valid set)
4. Performs well in real world
  - Change validation set or cost function
  
## Single number evaluation metric

precision and recall are good metrics but we should combine them into single number in case precision is better in one model but recall is better in the other.

## satisficing and optimizing metric

satisficing metric is conditional (e.g.; is run time of this model < 100ms). optimizing metric is one we are trying to improve (e.g.; accuracy). 

For example, if we have 3 cat classifiers, we will choose the one with the highest accuracy with a run time < 100 ms.

## train/dev/test distributions

dev and test sets should come from the same distribution (e.g.; if you have a cat classifier and have cats from different countries, dev and test set should grab samples from each country, rather than dev set consisting of samples from first half of countries, test set for second half)

## size of dev and test sets

98% train set, 1% valid set, 1% test set

## when to change dev/test sets and metrics

### orthogoanlization for cat pictures: anti-porn
suppose we have a lot of porn that is being classified as cat. Then we will have a separate step to remove porn instead of combining it into the classifier.

## summary

![summary](https://i.gyazo.com/5ad1bfcdaf4b13275ade64cca8e1782b.png)
* requires knowing the human level error % to compare against the train error %
