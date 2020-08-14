grad desc tends to oscillate when finding optimal value:
![wee](https://i.gyazo.com/d5447ffdaa14c81a728d17460e60803b.png)

- instead of updating weights with grads directly, we update with a weighted sum (vd) using previous vd's in computed in the minibatch:
![bowl](https://i.gyazo.com/62de879cd1ee0822be13f8ee947168bd.png)
  - analogy is the grads contribute "acceleration" to the optimal value and the vds contribute "friction", preventing it from oscillating as much, thereby getting the red line
  
## impl
- no need for bias correction when using grad desc with momentum
![impl](https://i.gyazo.com/e02c989f05179cd9019ed0bc78c843ab.png)
  - beta is the parameter for **exponentially weighted average**
