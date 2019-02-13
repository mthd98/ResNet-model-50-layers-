# ResNet-model-50-layers-

The details of this ResNet-50 model are:

Zero-padding pads the input with a pad of (3,3)
Stage 1:

The 2D Convolution has 64 filters of shape (7,7) and uses a stride of (2,2). Its name is "conv1".

BatchNorm is applied to the channels axis of the input.

MaxPooling uses a (3,3) window and a (2,2) stride.

Stage 2:

The convolutional block uses three set of filters of size [64,64,256], "f" is 3, "s" is 1 and the block is "a".

The 2 identity blocks use three set of filters of size [64,64,256], "f" is 3 and the blocks are "b" and "c".

Stage 3:

The convolutional block uses three set of filters of size [128,128,512], "f" is 3, "s" is 2 and the block is "a".

The 3 identity blocks use three set of filters of size [128,128,512], "f" is 3 and the blocks are "b", "c" and "d".

Stage 4:

The convolutional block uses three set of filters of size [256, 256, 1024], "f" is 3, "s" is 2 and the block is "a".

The 5 identity blocks use three set of filters of size [256, 256, 1024], "f" is 3 and the blocks are "b", "c", "d", "e" and "f".

Stage 5:

The convolutional block uses three set of filters of size [512, 512, 2048], "f" is 3, "s" is 2 and the block is "a".

The 2 identity blocks use three set of filters of size [512, 512, 2048], "f" is 3 and the blocks are "b" and "c".

The 2D Average Pooling uses a window of shape (2,2) and its name is "avg_pool".

The flatten doesn't have any hyperparameters or name.

The Fully Connected (Dense) layer reduces its input to the number of classes using a softmax activation. Its name should be 'fc' + str(classes).



Average pooling see https://keras.io/layers/pooling/#averagepooling2d

Here're some other functions we used in the code below:

Conv2D: See https://keras.io/layers/convolutional/#conv2d

BatchNorm: See https://keras.io/layers/normalization/#batchnormalization(axis: Integer, the axis that should be normalized (typically the features axis))

Zero padding: See https://keras.io/layers/convolutional/#zeropadding2d

Max pooling: https://keras.io/layers/pooling/#maxpooling2d

Fully conected layer: https://keras.io/layers/core/#dense

Addition: https://keras.io/layers/merge/#add
