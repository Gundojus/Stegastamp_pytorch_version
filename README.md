# StegaStamp using Pytorch
#### Contributers: Dan Epshtien and Neta Becker. Based on Jisong Xie's work

### Goals: 
* Develop a tool that encrypts information into a natural image based on existing code from Berkeley university. 
* Improve the algorithm performance in order to receive optimal output images along with good decoding performance. 

### Notations:
* Original image - the image before encoding
* Encoded image - The image after encoding
* Residual image - the image that is received by (Encoded image - Original image). meaning the values that were added to the original image during the encoding stage.

Using different loss functions, we managed to receive those results (Left to right: residual image, encoded image, original image):
![image](https://github.com/netabecker/Stegastamp_pytorch_version/assets/83274903/36e819c5-1109-4d81-93ef-205ad1da96d2)


### More notations:
* secret loss - The loss function of the encoding
* decipher indicator - Graph that depicts the number of images the decoder managed to decipher out of each batch of 4 images

As seen in the graphs below, there is a trade-off between the two - if secret loss value is low than the decipher indicator is low (meaning we are able to decipher less images out of each batch) and vice versa.
![image](https://github.com/netabecker/Stegastamp_pytorch_version/assets/83274903/c4756dfa-3ada-43fd-8961-16a9fdd4b91c)
