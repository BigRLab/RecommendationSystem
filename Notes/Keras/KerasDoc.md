# Keras Sequential model

Sequential moddes: linear stack of layers
## input shape
input_shape: first layer
  a tuple of integer or none

input_dim, input_length: 2D/ 3D layers
batch_size: specify a fixed batch size for inputs(for stateful recurrent networks)

## Compilation
configure the learning process
- optimizer:
- loss function: existed loss function(string identifier) or objective function
- list of metrics: string identifier or custom metric function

## Training
Keras model: trained on Numpy arrays of input data and labels
fit:
----
# API
In order to define complex models
create a chain from input to output, whose intermediate variables are tensor
Then package with model

## models are callable
a model will be in one line

## Multi-input and output models
----
# Keras model
1. Sequential model
2. the model class

model can get weights, load weights, draw the architecture and load the existed model weights
----
# Layers
