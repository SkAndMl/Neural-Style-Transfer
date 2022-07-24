# Neural Style Transfer

This repository is the implementation of **A Neural Algorithm of Artistic Style** by *Leon A.Gatys, et al.*. <br>

In their paper, they have combined several photographs with famous paintings thereby generating new art. This is done by finding the layers in a Convolutional
Neural Network that represent the style and contents of the photograph and the art to be combined.<br>

Once the style layers of the art has been obtained the style layers of the photograph is changed so that it's style represents the style of the art. This
is done by using gradient descent where we repeatedly train the style layers of the content image to slowly change it's values to the style layers of the 
art.

The level upto which one wants to combine is controlled by the number of epochs and the number of steps per epoch. Given below is a combination generated
from a *Labrador photograph* (content image) and a *Kandinsky painting* (style image). The model has been run for 10 epochs and in each epoch 100 steps have
been executed.
![nst_img](https://user-images.githubusercontent.com/86184014/180627707-418f8f25-2d49-4d57-96d9-ae821a288557.png)

The network used here is **VGG19** and the model only combines the Kandinski painting for now. <br>
The style layers of the VGG19 architecture have been identified as <br>
* *Block1_conv1*
* *Block2_conv1*
* *Block3_conv1*
* *Block4_conv1*
* *Block5_conv1*

There is only one content layer in this architecture and that is *Block5_conv2*. <br>

*More famous paintings and high resolution combinatios will be made available in the coming weeks*
