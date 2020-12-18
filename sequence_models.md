## rnn

## nlp

## basic sequence models
### sequence to sequence models
in machine translation:
![mt](https://i.gyazo.com/fb7029a9198ac1bea05c0cba038b42b5.png)

### image cpationing
![ic](https://i.gyazo.com/b3da6b9dffb3c1bbf51d4cd8f3cd0bf3.png)
  - cnn => rnn

## picking most likely sentence
![mt](https://i.gyazo.com/39dac5f325af72a7ad0629baff8857e4.png)
  - mt builds on langauge model by using an encoded x instead of bunch of zeros as input to decoder (produces y)
  - **encoder decoder arch**
![ml](https://i.gyazo.com/3fe2460626e8a4dbee1acb14f3ab06ff.png)
  - why not greedy search? suboptimal
![ml](https://i.gyazo.com/5bba9f8a1a6177d2378cabedeb781674.png)
  - solution: **beam search**
  
## beam search

![bs](https://i.gyazo.com/42198a01ef400961cacdc97bfbda6559.png)
  - first find 3 most likely first word options
  - we are now interested in 2nd most likely word for each of those 3 first word options:
  ![ex](https://i.gyazo.com/d6a78bdb01a56f10f82229748cb62f0a.png)
    - for example if we chose the first word "in", then we are interested in the most likely second word
  - more generally:
![bs](https://i.gyazo.com/a0602f73f9dfce4768f9f8fdc1977389.png)
  - one more step:
![bs](https://i.gyazo.com/00b26138e0b77b183100b5377f282d72.png)
  - greedy would be if B = 1, but we consider mutiple possibilities

problem: longer sentences have lower probability
solution: **length normaliziation**

### length normalization
![ln](https://i.gyazo.com/c10bc60dd14a0c00a91b5e3535fd065f.png)

note: Beam Search runs fast but is not guaranteed to find max prob sentrence

### error analysis
![ea](https://i.gyazo.com/42cd599f976df852800b8400897f4272.png)

## attention model
![prob](https://i.gyazo.com/472cf4394d7b80349224db9b80b3c508.png)

**sorry i wasnt paying attention to this video cause it was super boring (not trying to joke it was literally so boring)**
  - basic idea is "attention model allows a neural network to pay attention to only part of an input sentence while it's generating a translation, much like a human translator might"

![am](https://i.gyazo.com/0c746ce6325f5ff2868519ba2634c0d3.png)
  - we use bidirectional rnn
  - alphas are "how much attention y should focus on this word" and is generated by the activations from forawrd and backward
  - context depends on the alphas and is calculated by the weights sum of the alphas
  
![si](https://i.gyazo.com/43b04c3411e74c0a8aab8f091b8f774f.png)
  - same idea with the second word output
  - we basically have the alphas as attention weights

![math](https://i.gyazo.com/d62e2f8487100181971787973831bdae.png)

machine translation exmaple
![mte](https://i.gyazo.com/a6e33850e189c6159fbc47f7e8b60b25.png)

## speech recognition
-  another application of sequence to sqequence models
![audio](https://i.gyazo.com/25e8da3be991ab1b59fc2ee84b3cd0ce.png)
- we can use attention model:
!{am](https://i.gyazo.com/41d6dc53fe754cc9b750cb9568fbc6e4.png)

![ctc](https://i.gyazo.com/3d97be36fc4abfacb417f44092f2bfd7.png)
  - since audio is continuous and we can sample at times when there isnt a word sound, we can repeat characters 

## trigger word detection
![tw](https://i.gyazo.com/542611404b7167cbaaa466655e2e0266.png)
  - the blue underline sample is the trigger word being said; set 1 to all following lstm outputs; otherwise if not trigger word said then set to 0

 