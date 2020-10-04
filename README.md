# AutoEncoder LSTM : Unsupervised Learning of Video Representations using LSTMs
This is pytorch implmentation project of [AutoEncoder LSTM Paper](https://arxiv.org/abs/1502.04681) in vision domain.

## Training data
Original Paper experiment various dataset including [Moving MNIST](http://www.cs.toronto.edu/~nitish/unsupervised_video/).
This project only handle Movining MNIST Dataset.

- Dataset described in "[Unsupervised Learning of Video Representations using LSTMs](https://arxiv.org/abs/1502.04681)", 2015
>In Moving MNIST dataset, each video was 20 frames long and consisted of two digits moving inside a 64 × 64 pixcel.
>The digits were chosen randomly from the training set and placed initially at random locations inside the Image.
>Each digit was assigned a velocity whose direction was chosen uniformly randomly on a unit circle and whose magnitude was also chosen uniformly at random over a fixed range.

There is a well made Dataset in official Moving MSINST homepage. 
But the module which support to download dataset and preprocess image is used in this project for easy handling.
Module can be downloaded in this [[LINK]](https://github.com/tychovdo/MovingMNIST)

## Preprocessing
The images are contain only one channel.(NOT RGB Image)
So It doesn't need any complex preprocessing process.
Only scaling from 0 to 1 is applyed.

## Training Code
All Code is made with **Jupyter Notebook.**
Korean, English version is supported in this project.
Detail description is provided in [here](https://joungheekim.github.io/2020/10/11/code-review/) with korean.

## Result Visulization
### Reconstruction Task
This is reconstructed images from model when image sequence is used as a input
The model is trained to memorize shape of number in sequence images.
![](reconstruction6.gif)

### Prediction Task
This is predicted images from model when image sequence is used as a input.
The model is trained to catch velocity and shape of number in images.
![](prediction6.gif)

## Reference
- [[PAPER]](https://arxiv.org/abs/1502.04681) Unsupervised Learning of Video Representations using LSTMs, Srivastava at el
- [[GITHUB]](https://github.com/tychovdo/MovingMNIST) Moving MNIST Auto Download Module, tychovdo
- [[GITHUB]](https://github.com/bentrevett/pytorch-seq2seq) PyTorch Seq2Seq Sample, bentrevett
- [[DATASET]](http://www.cs.toronto.edu/~nitish/unsupervised_video/) Moving MNIST Dataset
