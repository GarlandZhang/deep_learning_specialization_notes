## word embeddings
- similar to face recognition encodings 

![rep](https://i.gyazo.com/eb0d5319003b1a8eebb1894bc85d38ef.png)
  - problem: its not known that apple is similar to orange compared to any other word choice
  - solution: we can represent features as an embedding to illustrate their similarity:  
![sim](https://i.gyazo.com/e6da4a714b8079d01bc9ee51ec623950.png)

heres a visual rep:
![visual](https://i.gyazo.com/b500be6bcde0445647df852405732f7d.png)

## applications
![named_entity](https://i.gyazo.com/5cad4039733b337ed72144a1de303514.png)

![transfer](https://i.gyazo.com/4b784647af101450ce8d65afd2c65163.png)

## analogies
![anal](https://i.gyazo.com/78ba470404329d1197f7dcf074611240.png)
  -man is to woman as king is to queen
  -in vector form:
 ![anal](https://i.gyazo.com/d1a4dc1bbaeb45d3f78f86c753a69528.png)

### cosine similarity
why are analogies useful?
![goal](https://i.gyazo.com/a60b27f9e1b896d6de31c6cbf93d447a.png)
  - so we can find the corresponding word 
 
## embedding matrix
  - this is our "weights"; we randomly initialize and use gradient descent to find the best values
![emb](https://i.gyazo.com/bd65097f74e67046da2f93552825c7e7.png)

## learning word embeddings
  - need to establish context to help model decide what model to output:
![conte](https://i.gyazo.com/ad9cbaf1a3655daa371057ff22143d2c.png)

## word2vec
our model arch:
![arch](https://i.gyazo.com/b1f881fe0325cc494cd6100b7e6341a8.png)
  - called **skip-gram model**
problems:
![prob](https://i.gyazo.com/9d1fe1dd00478caeb6b88a89c7a97e52.png)
  - have to sum over all words in vocab
  
## negative sampling
![def](https://i.gyazo.com/a7f58882480b346f459f72d2cdece312.png)
  - choose k negative samples (where context + word does not make sense together)
  
solution to word2vec problem:
![neg](https://i.gyazo.com/8eb9a78e940e096e4ab9a6dc7e5728c2.png)
  - whereas before we train 10000 units in the softmax layer, we only train k + 1 (k randomly selected negative samples, 1 being the positive sample) of the units in each iteration

### selecting negative examples
[prob](https://i.gyazo.com/4f4217d56ff3329bdf5e02bcc62b6bbb.png)
  - prob of choosing the word is based on frequency of the word used, f
    
## gloVe word vectors (global vectors for word representations)
![glove](https://i.gyazo.com/c1461515f59686bc9d9390c1f84c86c8.png)
  - in our case, xij = xji because proximity is relative; if we talked about 1 being before the other then this equation not true
  - idea behind minimization cost function is ensuring that log(Xij) aka log of frequency is approx theta * embedding
![cfn](https://i.gyazo.com/7791de06cb024d99c4635ad0a1208b01.png)
[CORRECTION]
![corr](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Wb1_QMhfEemRPArJHNevzg_678507a1c83ea1d6ad8dcf1b481a705a_Glove.png?expiry=1597968000000&hmac=cMDj5_b85bpuFmEwb1BMGk4OdH7V08LfloztNjdB_64)
  - we can ubdate embedding after running g.d. by taking average of the new weight and theta weight
  
## sentiment classification
  - given sentence, output rating from 1 to 5:
![sent](https://i.gyazo.com/02eb72b0b31b85d11f2c69a1a248f967.png)
  - problems: ignore word order which can change interpretation of actual sentiment
  - solution: use rnn
### rnn sentiment classification
![rnn](https://i.gyazo.com/b59410698daf28895bd3bfab0a645ee5.png)

## debiasing word embedddings
  - problem of bias: 
![bias](https://i.gyazo.com/d9681076524a8f42caa93f678b4e1cf3.png)

solution:
![sol](https://i.gyazo.com/d64a5e9235eb9a01e857df0af1f01a5c.png)
  - on high level, if grandmothers babysit more than grandathers, we can neutralize this bias by moving babysitter to axis and equalizing distance grandmother and grandfaterh have to axis therefore babysitting is equidistant to both granmdother and grandfather
