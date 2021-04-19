# Artificial-Neural-Network-ANN-implementation-on-Breast-Cancer-Dataset
To implement artificial neural network, I have used Keras which is a high-level Neural Networks API built on top of low-level neural networks APIs like Tensorflow and Theano. As it is high-level, many things are already taken care of therefore it is easy to work with and a great tool to start with.

After importing useful libraries I have imported Breast Cancer dataset, then first step is to separate features and labels from dataset then we will encode the categorical data, after that we have split entire dataset into two part: 70% is training data and 30% is test data. After that, we will scale the both training and testing datasets.

Initialize the Artificial Neural Network (ANN):-

The model needs to know what input shape it should expect. For this reason, the first layer in a Sequential model (and only the first, because following layers can do automatic shape inference) needs to receive information about its input shape. There are several possible ways to do this:

input_dim - number of columns of the dataset
output_dim - number of outputs to be fed to the next layer, if any
activation - activation function which is ReLU in this case
init - the way in which weights should be provided to an ANN
The ReLU function is f(x)=max(0,x). Usually this is applied element-wise to the output of some other function, such as a matrix-vector product. In MLP usages, rectifier units replace all other activation functions except perhaps the readout layer. One-way ReLUs improve neural networks is by speeding up training. The gradient computation is very simple (either 0 or 1 depending on the sign of x). Also, the computational step of a ReLU is easy: any negative elements are set to 0.0 – no exponentials, no multiplication or division operations.

Optimizer:-

Just to improve the performance of model we have also applied some optimizer. Optimizer is chosen as ‘adam’ for gradient descent. ‘Binary_crossentrop’y is the loss function used. Cross-entropy loss, or log loss, measures the performance of a classification model whose output is a probability value between 0 and 1. Cross-entropy loss increases as the predicted probability diverges from the actual label. So, predicting a probability of .012 when the actual observation label is 1 would be bad and result in a high loss value. A perfect model would have a log loss of 0.


