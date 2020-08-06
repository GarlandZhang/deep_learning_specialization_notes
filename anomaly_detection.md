to determine if a data point is an outlier

![ex](https://i.gyazo.com/50f41e6e6ed693be5dca5c1d77b1551b.png)

we can also use **density estimation**:

![de](https://i.gyazo.com/622c5e42fa56b0bf0391900722804ebc.png)

more detection examples:

![exs](https://i.gyazo.com/f4e77292c80e2d8182d86f7f862166a8.png)

## algorithm

first note that:
![ind](https://i.gyazo.com/2798a08802b0a3da4069e889cc7e811f.png)
  - all features are (presumably) independent, hence we can multiply the model outputs toegether
  - p is the gaussian probability density function
  
![algo](https://i.gyazo.com/824cfefea92f15a5bc3ddae1ff0b731b.png)
  -  idea is we classify an anomoly if its outside of the usuaal gaussian distributions
  
![dis](https://i.gyazo.com/14e06d2598b7243de6777cf862bca115.png)
  - the bottom graph illustrates p(x), a density visualization of the above graph
  - anything thats is on the "flat" area of the p(x) model will most likely have <= E, therefore considered an anomoly!
  
  
## process of developing a specific application of anomaly detection

- like any learning algo, we need train/valid/test sets with labeled data (since we are using a classifier)

![engine](https://i.gyazo.com/c32a53950bb7d199d20dd5c1cd8b48cb.png)

for eval:
![eval](https://i.gyazo.com/eeb30595c481c437a1ca750c97c8c434.png)

note: **classification accuracy** is not a good measure due to skewed classes, so predicting y=0 will be the best choice 

## anomaly detection vs supervised learning

why not just use a neural network or supervised learning algoirthm instead?

![comp](https://i.gyazo.com/b9de679d6197f9c115590d587cbb5e6f.png)
  -in summary, use anomaly detection for "unusual" classification, and supervised otherwise
  
## common problems + choosing features

- not all features are gaussian; so we need to make them look gaussian; can be done using log, sqrt,  ^ 1/3, or log(x + [constant])
![make_g](https://i.gyazo.com/af0f0d0b7266edb555196e98074768ea.png)

- want p(x) for anomalies should be < Epsilon but what if it is too large?
![large](https://i.gyazo.com/de557e4e963d7aab2e16a4b4088074cc.png)
- it helps to look at the specific example (since there arent many) to determine the new feature (x2) to prevent misclassification:
![x2](https://i.gyazo.com/81e7e8571e7916a71d99c55d75ab503e.png)


- finally choose features that take on unusually large or small values in event of anomally:

![cpu](https://i.gyazo.com/27743fb62be18b75b8a72b1af0768129.png)
