# CoinCounter
This is a coin counter using digital image processing.

Basically, the project is divided in four modules:

* *'segmentador'*: breaks a picture with a lot of coins in small images, each one with only one coin in the center. Example of input and output:

Input:
![input1](https://github.com/DenisMedeiros/CoinCounter/raw/master/completas/1.jpg)

Output (only one of 12 small images):
![output2](https://github.com/DenisMedeiros/CoinCounter/raw/master/treinamento/100/1.jpg)

* *'calibrador'*: uses part of the small images generated by previous module to train a Artificial Neural Network (ANN), in order to classify the coins correctly. For this, the descriptors of each image containing a coin are the following ones:
  - Width and height of the image
  - Histogram of the hue channel of the image
  - 7 hu moments
  
* *'validator'*: uses other small images obtained by the first module in order to validate the classification of the ANN. 

* *'contador'*: using the results of the 'calibrador', it reads a picture containing some several coins and count the amount of money there. 
