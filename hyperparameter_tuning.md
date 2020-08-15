- try random values

![grid](https://i.gyazo.com/f1d9083f7a264237cbbbe8cbc08727db.png)

- coarse to fine:

![coarse](https://i.gyazo.com/3dafede32a9c996107ae2910ee526e87.png)
  - after sampling, focus on a smaller section that has been performing best
  
## using an appropriate scale for hyperparameters
  - dont do binary search when you can do logarithmic!
  ![log](https://i.gyazo.com/e565911b0ed59a6b94f77bdacc8f9609.png)
  
## in practice

"babysitting": keep updating the model and tune hyperparameters manually
"parallel": train models in parallel with different hyperparameters
