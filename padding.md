- pixels in the edges/corners are only exposed to a few kernels
- in adddition, the size of the tensor shrinks
- solution: we can use padding to solve both problems:


![paddi](https://i.gyazo.com/a4b12fc6f6a4be4904aa25cfea809cf6.png)
  - no paddding is aka "valid"
  - padding to preserve original shape is aka "same"
 
