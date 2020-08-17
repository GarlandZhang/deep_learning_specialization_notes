![prob](https://i.gyazo.com/70f3249ac80b8a9e001b0e3f445d21b6.png)

## neural style transfer

- uses pretrained VGG19 network to get the relevant feature maps. Applies gradient to image and not to any model

### cost function
- to balance content and style, we incluide both losses ![loss](https://i.gyazo.com/6b76b4443701f54f0f260ad5be0c2aee.png)
![cost](https://i.gyazo.com/2fc0ef3502d76c2c7a9c82f552eb2f4d.png)

#### content cost function
- use MSE between the activations in the same layer in VGG19
![content](https://i.gyazo.com/ec3b2f02c184d7136884d684a6a93a01.png)

#### style cost function
![style](https://i.gyazo.com/95fe07501db4548a38a7d511001c96b9.png)
  - we relate style across the activations of the same layer by using gram matrix
![matri](https://i.gyazo.com/96992b254e33984d49d9919271c58d92.png)

![cost](https://i.gyazo.com/a849d9b0840501a1473894df51cbc45b.png)
  - by layer, it refers to whicever layer we use in the convnet (i.e. vgg19)
  


## fast neural style transfer

- identical loss function but instead applies to a feed forward network. see **https://towardsdatascience.com/towards-fast-neural-style-transfer-191012b86284** for more detail.

- apparently is not as good as neural style transfer and is limited to the styles it was trained on
