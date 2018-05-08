# Assignment 3

## Regularization In Machine Learning

It is a process of introducing additional information to prevent overfitting or is a technique used in an attempt to solve the overfittin problem in statistical models.

### DropOut

It refers to dropping out units in neural network. Technically, At each training stage, individual nodes are either dropped out of the net with probability 1-p or kept with probability p, so that a reduced network is left; incoming and outgoing edges to a dropped-out node are also removed.

We need DropOut to prevent over-fitting. A fully connected layer occupies most of the parameters, and hence, neurons develop co-dependency amongst each other during training which curbs the individual power of each neuron leading to over-fitting of training data.

### Label Smoothing

It is a nice technique to regularize models trained with cross-entropy error.

Label smoothing regularization estimates the marginalized effect of label-dropout during training, reducing overfitting by preventing a network from assigning full probability to each training example and maintaining a reasonable ratio between the logits of the incorrect classes.

It can be exhaustively evaluate on 6 commong benchmarks:

1. Image Classification (MNIST and Cifar-10),
2. Language Modeling (Penn Treebank),
3. Machine Translation (WMT’14 English-to-German), and
4. Speech Recognition (TIMIT and WSJ)

## Normalization

It is an example of preprocessing data to remove or reduce the burden from any machine learning (ML) to learn certain invariants i.e, things which make no difference in the meaning of the symbol, but only change the representation.

### Batch Normalization

Batch Normalization helps relaxing neural networks including deep networks in careful tuning of weight initialization and learning parameters.

Some of the benefits are:

1. Networks train faster
2. Allows higher learning rates
3. Makes weights easier to initialise
4. Makes more activation functions viable
5. Simplifies the creation of deeper networks
6. Provides some regularisation

### Layer Normalization

It is very similar to batch normalization, acts on a per layer per sample basis, where the mean and variance are calculated for a specific layer for a specific training point.

In this normalizatoin, Input values for different neurons in the same layer are normalized without consideration of mini batch. All of the summed inputs to the neurons in a layer is on a single training case.

### Weight Normalization

Salimans and Kingma introduce weight normalization, a reparameterization of network weights in order to improve training.

A reparameterization of the weight vectors in a neural network that decouples the length of those weight vectors from their direction. By reparameterizing the weights in this way we improve the conditioning of the optimization problem and we speed up convergence of stochastic gradient descent.

## Optimization

Optimization formulations and methods are proving to be vital in designing algorithms to extract essential knowledge from huge volumes of data.

### SGD

SGD also stands for Stochastic Gradient Descent, performs a parameter update for each training example. It can make erratic updates on non-smooth loss functions. It is usually much faster technique. It performs one update at a time.

### RMSProp

It is an unpublished, adaptive learning rate method. It has been developed independently around the same time stemming from the need to resolve Adagrad's radically diminishing learning rates.

RMSprop as well divides the learning rate by an exponentially decaying average of squared gradients

### Adam

The **Adam optimization algorithm is an extension to stochastic gradient descent that has recently seen broader adoption for deep learning applications in computer vision and natural language processing.

Some benefits of using Adam on non-convex optimization problems:

1. Straightforward to implement.
2. Computationally efficient.
3. Little memory requirements.
4. Invariant to diagonal rescale of the gradients.
5. Well suited for problems that are large in terms of data and/or parameters.
6. Appropriate for non-stationary objectives.
7. Appropriate for problems with very noisy/or sparse gradients.
8. Hyper-parameters have intuitive interpretation and typically require little tuning.

### Cyclic Learning Rates

It is one of the most important hyperparameters to be tuned and holds key to faster and effective training of neural networks.

Cyclic Learning Rates, practically eliminates the need to experimentally find the best values and schedule for the global learning rates. Instead of monotonically decreasing the learning rate, this method lets the learning rate cyclically vary between reasonable boundary values.
