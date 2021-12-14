# Liminal-GAN

##### PyTorch implementation of DCGAN mainly following [this tutorial](https://pytorch.org/tutorials/beginner/dcgan_faces_tutorial.html)

### First Draft 12/6/2021:

Data gathered using ripme on [r/LiminalSpace](https://www.reddit.com/r/LiminalSpace/) and [@SpaceLiminalBot](https://twitter.com/SpaceLiminalBot)

Gathered ~4,000 images total of both interior and exterior Liminal Spaces

### Second Draft 12/14/2021:

Added extra convolutional layers in Generator and Discriminator to increase image size frmo 64x64 to 128x128. This originally made the model unable to converge so I implemented One Sided Label Smoothing (Changing "real" label from 1 to 0.9) from [Improved Techniques for Training GANs](https://arxiv.org/pdf/1606.03498.pdf)

Also compressed images and resized before importing which greatly reduced the train time for the model. Was able to run 220 epochs before I gave up on seeing improvement. 

Next step is to implement feature matching from the Improved Techniques paper.

## To Do:
- Try implementing StyleGAN and ADA
