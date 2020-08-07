map reduce is a parallel processing technique to perform batch gradient descent by breaking up the training examples and calculating these substes:

![map](https://i.gyazo.com/a43834baec7d330961c5034ee3d111f6.png)

high level diagram:

over multiple machine
![diag](https://i.gyazo.com/96ac5ac5b616dd93b9906bc2313729ee.png)

over multiple cores (same idea)
"The advantage of thinking about MapReduce this way, as paralyzing over cause within a single machine, rather than parallelizing over multiple machines is that, this way you don't have to worry about network latency, because all the communication, all the sending of the back and forth, all that happens within a single machine."

![cores](https://i.gyazo.com/141d17c960bc45bbf2a5ec1ae7bd4a55.png)

