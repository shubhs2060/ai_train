Neural Network

A Neural Network is essentially a series of mathematical transformations that convert input data into output predictions.
Each layer in the network transforms the data it receives and passes it to the next layer.

Input Example: [x1, x2, …, xn]

Output: The model learns to map inputs (x values) to outputs (y values) during training. Once trained, it can predict a new y for a given new x.

Example: Linear Neural Network

A simple neural network can be represented as

y=Wx+b

Here:

W = weight parameters (learned during training)

b = bias term

x = input

y = output (prediction)

If we use two layers, it would look like this:
Each layer has its own W and b

Layer 1: Takes the input x, applies some weights W1, and outputs L1.


L1=W1x+b1

Layer 2: Takes L1, applies another transformation with weights W2, and outputs L2.

L2=W2L1+b2

Finally, the output layer uses L2 to make the prediction.

Transformer

The Transformer architecture was introduced to handle sequence-based transformation tasks (like language translation). It quickly became the foundation for most Large Language Models (LLMs) because of its efficiency and accuracy.

Transformers are made of two parts:

Encoder

Decoder

However, most modern LLMs (like GPT models) use only the Decoder architecture.

How the Transformer Decoder Works

Input: "How are you"

Embedding Layer: Converts words into numerical vectors (embeddings).

Transformer Decoder: Processes these embeddings through multiple attention and feed-forward layers, outputting a sequence of vectors.

Output Processing:

We typically use the last output vector to predict the next word.

Each vector represents probabilities across all words in the vocabulary.

For example, suppose the final output vector produces probabilities like:

[223, 244, 212, 455]


Mapping these to words via the vocabulary:

[do, to, sleep, today]


Since “today” has the highest probability, the model outputs “today.”