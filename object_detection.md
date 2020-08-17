combines object localization + landmark detection

## sliding window
  - slide submatrix with some stride to find iamge
  - problem: computationally inefficient, fixed size squares

### impl
first we consider a fully connected (FC) layer as a 1x1xF convolutional layer:
![conv](https://i.gyazo.com/4511bac4c2fdb4e22d7247d304018e31.png)

since we pass a cropped image as input into the CNN, we have:
![impl](https://i.gyazo.com/5fb9312ec79de9d8b2d9001978a3c8e6.png)
  - but this is inefficient as we have overlapping computations with the next window. instead:
  
![impl](https://i.gyazo.com/dade2d606ea030781aaeadae391d0d8e.png)
  - here we run on the entire image size and the resulting 2x2x4 gives us all the windows! the blue pixel is the same result as the above image
