# **Image Classification on Fashion-MNIST** #

In this notebook, we build a convolutional neural network on tensorflow to classify Fashion-MNIST, which is a dataset of Zalando's article images (https://www.kaggle.com/zalando-research/fashionmnist). This dataset consists of a training set and a validation set, each of which contains 60,000 and 10,000 examples, respectively. Each example is a 28x28 grayscale image, assigned labels from 10 different classes. Fashion-MNIST is a direct drop-in replacement for the original MNIST digit dataset for benchmarking machine learning algorithms. It shares the same image size and structure as training and testing splits.

Each training and test example is assigned to one of the following labels:

Label Description

*  T-shirt  - 0 <br />
*  Trouser  - 1 <br />
*  Pullover - 2 <br />
*  Dress    - 3 <br />
*  Coat     - 4 <br />
*  Sandal   - 5 <br />
*  Shirt    - 6 <br />
*  Sneaker  - 7 <br />
*  Bag      - 8 <br />
*  Ankle boot - 9 <br />

## **Evaluation and Results** ##

A simple architecture is used to fit the data into the model, which has fewer than 35,000 parameters and could execute on a low-end CPU with less memory. The tandem of a convolutional layer and max-pooling is used to extract features corresponding to different classes. The resulting feature is fed into a fully connected layer for prediction. Dropout regularisation is also implemented between dense layers to avoid overfitting. For a detailed definition, check the model definition provided in the notebook. <br />
Summary of the Model.

![parameter](https://user-images.githubusercontent.com/58718943/210721119-3e62db5d-b51a-407c-9abe-18fc9738d319.jpg)
<br />
Furthermore, because Y<sub>i </sub> are integers and not one-hot encoded, "sparse categorical cross-entropy" is used for the determination of loss, and the Adam algorithm is used for the optimization of parameters.
<br />
After training for 20 epochs, the model achieved an accuracy of 92% on the training dataset and 88% on the validation dataset.
