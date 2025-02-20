# Handwriting_Detection using TensorFlow

Handwritten Text Recognition (HTR) system implemented with TensorFlow (TF) and trained on the IAM off-line HTR dataset. This Neural Network (NN) model recognizes the text contained in the images of segmented words.

The Deep Learning algorithms used for the Handwriting detection were:
1.	5 CNN (2-D Convolutional Neural Network) layers
2.	2 LSTM (Long Short Term memory) layer – part of RNN network
3.	1 CTC loss and decoding layer

The word decoding algorithm choices in the program are:
1. Best path coding
2. Vanilla beam search

The data-loader requires "words" folder to be added in the data/ directory.

1.	Register for free here: http://www.fki.inf.unibe.ch/databases/iam-handwriting-database
2.	Download words/words.tgz.
3.	Download ascii/words.txt.
4.	Put words.txt into the data/ directory.
5.	Create the directory data/words/.
6.	Put the content (directories a01, a02, ...) of words.tgz into data/words/.

The below image is used for inference of the model:

![](data/test.png)

For an untrained (Ground Zero) model, output is:

1. Recognized: little
2. Probability: 0.522
3. Validation character error rate: 17.66 %

For a trained model with 2 epoches (iterations), output is:
1. Recognized: little
2. Probability: 0.567
3. Validation character error rate: 15.75 %

For a trained model with 6 epoches (iterations), output is:
1. Recognized: little
2. Probability: 0.653
3. Validation character error rate: 15.20 %

Since the training process takes a long time to complete, the model has been run for maximum 6 epoches, wherein with each iteration there is an improvement in performance. This model will perform very well when the whole training process is completed.
