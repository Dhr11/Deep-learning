# Deep-learning
 ## 1: A Detailed View to MNIST Classification 
A fully-connected net for MNIST classification. 
With 5 hidden layers each of which is with 1024 hidden units. 

PCA and TSNE Results on last hidden layer
![PCA LAST LAYER]( https://github.com/Dhr11/Deep-learning/blob/master/mnist_pca_lastlayer.png)
![TSNE LAST LAYER]( https://github.com/Dhr11/Deep-learning/blob/master/mnist_tsne_lastlayer.png)

Score of about 98.4 percent on classification of images.
Used He initialization for weights and biases. 

## 2: Speech Denoising Using Deep Learning
Libraries used for sound: Librosa, mainly for transferring to and from frequency domain using stfft and istft.

### Done with 4 different approaches 
 
1.	Fully connected with 5 hidden layers each of which is with 1024 hidden units. 
2.	1-D Convolutional method with 2 cnn layers and pooling and dropout
3.	2-D cnn with maxpool and dropout
4.	Lstm approach. Predicting Ideal Bindary Masks using model and then reconstructing audio


## 3: Network Compression Using SVD

Built a baseline model, 5 layer fully connected model
Singular Value Decomposition (SVD) can compress the weight matrices, so compressed the 5 of the 6 weight matrices, leaving the last layer one out.
Each matrix is deconstructed in to matrices U, S and V
Now we can select the most relevant D features from these matrices by taking subsets from them.
Below is the image, showing the changes in accuracy of the quantized model as we change the number of features columns selected.
![Quantization scores]( https://github.com/Dhr11/Deep-learning/blob/master/network_quantization.png

 
##4: Speaker Verification

The training matrix is ordered by speakers. Each speaker has 10 utterances, and there are 50 such speakers (that’s why there are 500 rows). Similarly, the test set has 20 speakers, each of which is with 10 utterances
Each mini batch, has : 
Positive samples- Sample L pairs of utterances from the ten utterance for a speaker
Negative samples - Randomly sample L utterances from the 49 other training speakers. Using them and the ten utterances of the first speaker, form another set of L pairs
Train a Siamese network that tries to predict 1 for the positive pairs and 0 for the negative ones


