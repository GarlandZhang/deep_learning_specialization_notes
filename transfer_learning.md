- reuse an existing model (with trained weights) by just changing the final layer (and the weights from the second last layer to the last layer) then add your own layer
- this works because model already learned the "structure" of what images look like

![when](https://i.gyazo.com/700c636d072e9c13950a5734fa583225.png)

## improving efficiency
  - since we freeze layers, then for any x, we have some y value. then we can store all these y values and just return these instead of having to pass x through the frozen layers to recompute y!
  
  
