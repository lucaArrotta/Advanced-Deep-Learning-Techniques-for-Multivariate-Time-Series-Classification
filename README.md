# Advanced Deep Learning Techniques for Multivariate Time-Series Classification

This repository contains the implementation of some advanced deep learning techniques for multivariate 
time-series classification. The application domain is sensor-based Human Activity Recognition where
the goal is to detect the activities performed by users (e.g., running) based on sensor data collected
through their mobile devices, like smartwatches and smartphones.

<hr>

### Neuro-Symbolic AI: 

The Neuro_Symbolic_AI.ipynb notebook contains the implementation of a Neuro-Symbolic AI technique that
infuses human commonsense knowledge about activity recognition (e.g., walking requires that the current
user's speed is positive) into a deep neural network. 

This allows reducing the labeled training data
required to learn such a knowledge in a data-driven fashion, thus increasing the recognition rates compared
to a fully-supervised baseline.

This Neuro-Symbolic AI method is based on the one proposed in this research paper: 
[Neuro-Symbolic Approaches for Context-Aware Human Activity Recognition](https://arxiv.org/abs/2306.05058)

<hr>

### Transfer Learning

The Transfer_Learning_and_Self_Supervised_Learning.ipynb notebook contains the implementation of
a deep neural network that is initially pre-trained on the labeled data of some users; 
this model is then personalized to recognize the activities of a new user:
the feature extraction layers of the model are fine-tuned on the small amounts of labeled
training data available from the new user (also performing activities not considered during pre-training).

This approach allows improving the recognition rates of a baseline fully-supervised model only trained on 
the labeled data used to fine-tuned the first model.

<hr>

### Self-Supervised Learning
	
The Transfer_Learning_and_Self_Supervised_Learning.ipynb notebook also contains an implementation of 
the Sim-CLR framework to pre-train a deep neural network on huge amounts of unlabeled data; 
such a model is then fine-tuned on small amounts of labeled data.

This approach allows improving the recognition rates of a baseline fully-supervised model only trained on 
the labeled data used to fine-tuned the first model.

This implementation of Sim-CLR is based on the one proposed in this research paper:
[Exploring Contrastive Learning in Human Activity Recognition for Healthcare](https://arxiv.org/abs/2011.11542)

