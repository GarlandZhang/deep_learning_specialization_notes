recurrent neural networks
cheat sheet: ![](https://stanford.edu/~shervine/teaching/cs-230/cheatsheet-recurrent-neural-networks)

## notation

![vocab](https://i.gyazo.com/4dec741ef8e9444393f3194e96345c57.png)

**read up to forward prop section then come back to understand this notation**



## problems w/ standard NN

![standard](https://i.gyazo.com/65baa17c4a607e289981f40d32d797e8.png)

## arch

![arch](https://i.gyazo.com/127ac2b027b106244bb8fe0379129909.png)
  - goal: determine if the word is a name or not (each y^ is 0 or 1)
  - problem: does not take info about words that come after the current word:
  ![prob](https://i.gyazo.com/1f90fe1ce486d4112a7c8f24444f3d9a.png)

## forward prop

![for](https://i.gyazo.com/a3d2ad4306df77bd6896f10c8ab46dd3.png)

## loss fn

![backprop](https://i.gyazo.com/31587b1be009d3f4a68078f4104db721.png)

## backward prop
  - backprop from y is same
  - backprop from recursive step is carried over to previous recursive step
  
## applications
![ex](https://i.gyazo.com/7ca33465cf1713d9093307c6e364ede6.png)
![ex](https://i.gyazo.com/9a2e9f68013d68c19ad556fa67d6c287.png)
  - we've already seen one instance of many-to-many from above

![ex](https://i.gyazo.com/cff96ed05411faf262d18ae4da93d912.png)

## summary

![summ](https://i.gyazo.com/363f5b8368f2b90c9a10a2f9af3283d5.png)

## language modelling

![define](https://i.gyazo.com/f9e99ffd4eaab63cbc049550fcea073d.png)

![rnn](https://i.gyazo.com/3cf46390b0c7693a6949d51a1406db7b.png)
  - this model predicts next word based on probability 
  - notice we feed the correct output instead of the passed in output (i think for training)
  
### loss function

![loss_fn](https://i.gyazo.com/3d3d7982759f29614b8552d53344074b.png)

## sampling sequences
![sample](https://i.gyazo.com/7dc6964cd9a9c37192be98240f2da236.png)
  - used to get am idea of what the sequence model has learned
  - instead of feeding the correct output, we pass the previous output as input:
  - the sequence ends when EOS token is sampled OR just fix length:

with characters instead of words:
![char](https://i.gyazo.com/19845462328eb6bfaaaeef4066007eb2.png)

we can generate sentences!
  
## exploding gradients
  - solution: **gradient clipping*: limit how much gradient to be

## vanishing gradients with rnns
  - some words have long-term dependencies (e.g.; 'cat...was' vs 'cats...were')
  - in general, y^ outputs are affected by "recent" inputs and not really from far inputs
  ![vanishing](https://i.gyazo.com/529ef9d3d76adc668abc2a41bea3aa51.png)
  
## gated recurrent unit (GRU)
[DO NOT UNDERSTAND]
  - gamma is the gate is responsible for when to update the memory cell
    - 1 = update
    - 0 = dont update
  
## Long Short Term Memory (LSTM)
  - more powerful than GRU
![LSTM](https://i.gyazo.com/b9f9c9ab2966d32ad7d5a1206ccdac90.png)
  - activation and input is used to compute forget, update, and output gates
    - a "peephole connection" is a variation of the formula where it also depends on c<t-1>
  - c is our "memory"
  
## bidirectional RNN
![bi](https://i.gyazo.com/d500044c00d3192c6b097a0e63c54552.png)
  - so far all RNNs are unidirectional (left to right)
  - bidirectional takes information from previous tokens and after tokens
  - disadvantage: needs information from the entire sentence before predicting
  
## deep rnns
![deeo](https://i.gyazo.com/41601051c7d55314d337d8bed154d4c7.png)
