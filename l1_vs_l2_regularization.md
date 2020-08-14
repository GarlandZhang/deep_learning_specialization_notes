name origination:

![naming](https://miro.medium.com/max/700/1*44D2AeENsOASBjxWA-XcFw@2x.png)

model used for l1 and l2 can be the same but the cost function is different:

![cost](https://miro.medium.com/max/646/1*1zCcVuEOPi64mjkkF6Uj7w@2x.png)

grads:

![grad](https://i.gyazo.com/7304fba76a27705c21191ae6e2a5756e.png)

Apart from H, the change in w depends on the ±λ term or the -2λw term, which highlight the influence of the following:
1. sign of current w (L1, L2)
2. magnitude of current w (L2)
3. doubling of the regularisation parameter (L2)

##  L1’s effect on pushing towards 0
"If w is positive, the regularisation parameter λ>0 will push w to be less positive, by subtracting λ from w. Conversely, if w is negative, λ will be added to w, pushing it to be less negative. Hence, this has the effect of pushing w towards 0."
"This is of course pointless in a 1-variable linear regression model, but will prove its prowess to ‘remove’ useless variables in multivariate regression models. You can also think of L1 as reducing the number of features in the model altogether. "
  - recall reducing number of features simplifies model complexity, thereby preventing overfitting
  
note: While L1 has the influence of pushing weights towards 0 and L2 does not, this does not imply that weights are not able to reach close to 0 due to L2.

### more on L2
- also called "weight decay" because in addition to gradient update, it also reduces magnitude of the weights
![decay](https://i.gyazo.com/e8526e804c4f911017dd3cdbb10bbf06.png)


