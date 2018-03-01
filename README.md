# Welcome to sentence space

You can find an introduction to this project, with examples and live demos, [here](https://www.robinsloan.com/voyages-in-sentence-space).

This is a server designed to provide a couple of interesting artifacts. The core of it is a variational autoencoder that embeds sentences into a continuous space; as a result, you can select a point anywhere in that space and get a (more or less) coherent sentence back.

Once you've established this continuous sentence space, what can you get from it?

1. *Sentence gradients*: smooth interpolations between two input sentences.
2. *Sentence jitters*: clouds of alternative sentences closely related to an input sentence.

These are very weird artifacts! If you try to write a sentence gradient by hand, you'll find it's very difficult. Are they useful? Possibly not. Are they _interesting_? Definitely!

Again, you'll find a ton more context and exploration in [this post](https://www.robinsloan.com/voyages-in-sentence-space).

This code isn't quite turnkey, but if you're willing to tinker a little, you should be able to get up and running, training your own models and serving your own gradients, jitters, and who-knows-what-else.

Requirements include:

* Python 2.7
* Theano and its dependencies, including Numpy
* `[sentencepiece](https://github.com/google/sentencepiece)` (if you want to use the included, pretrained model)
* `[wordfilter](https://github.com/dariusk/wordfilter)`

This project is forked from `[stas-semeniuta/textvae](https://github.com/stas-semeniuta/textvae)`, which is the code for the paper ["A Hybrid Convolutional Variational Autoencoder for Text Generation"](https://arxiv.org/abs/1702.02390) by Stanislau Semeniuta, Aliaksei Severyn, and Erhardt Barth. I'm indebted to Semeniuta, et. al., for their skill and generosity. If I have tinkered slightly, it is because I stood on the shoulders of smart people.

I'm indebted also to [`@richardassar`](https://github.com/richardassar), whose improvements allow this server to provide results at interactive speeds.

You can find Semeniuta et. al.'s original README in (you guessed it) `ORIGINAL-README.md`.