# Regularization In Machine Learning

It is a process of introducing additional information to prevent overfitting or is a technique used in an attempt to solve the overfittin problem in statistical models.

## DropOut

It refers to dropping out units in neural network. Technically, At each training stage, individual nodes are either dropped out of the net with probability 1-p or kept with probability p, so that a reduced network is left; incoming and outgoing edges to a dropped-out node are also removed.

We need DropOut to prevent over-fitting. A fully connected layer occupies most of the parameters, and hence, neurons develop co-dependency amongst each other during training which curbs the individual power of each neuron leading to over-fitting of training data.

## Label Smoothing

It is a nice technique to regularize models trained with cross-entropy error.

Label smoothing regularization estimates the marginalized effect of label-dropout during training, reducing overfitting by preventing a network from assigning full probability to each training example and maintaining a reasonable ratio between the logits of the incorrect classes. 

It can be exhaustively evaluate on 6 commong benchmarks:
1. Image Classification (MNIST and Cifar-10),
2. Language Modeling (Penn Treebank),
3. Machine Translation (WMT’14 English-to-German), and
4. Speech Recognition (TIMIT and WSJ)


# Normalization

It is an example of preprocessing data to remove or reduce the burden from any machine learning (ML) to learn certain invariants i.e, things which make no difference in the meaning of the symbol, but only change the representation.

## Batch Normalization

Batch Normalization helps relaxing neural networks including deep networks in careful tuning of weight initialization and learning parameters.

Some of the benefits are:
1. Networks train faster
2. Allows higher learning rates
3. Makes weights easier to initialise
4. Makes more activation functions viable
5. Simplifies the creation of deeper networks
6. Provides some regularisation

## Layer Normalization

It is very similar to batch normalization, acts on a per layer per sample basis, where the mean and variance are calculated for a specific layer for a specific training point. 

In this normalizatoin, Input values for different neurons in the same layer are normalized without consideration of mini batch. All of the summed inputs to the neurons in a layer is on a single training case.

## Weight Normalization