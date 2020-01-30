---
title: "DP-CGAN: Differentially Private Conditional GAN on TensorFlow 2 explained"
summary: "I describe a TF 2 implementation of a Differentially Private Conditional GAN, originally described on Torkzadehmahani et al. 2019."
date: "2020-01-29"
all_day: true
authors: ["admin"]
tags: ["Differential Privacy", "GAN", "TensorFlow"]
featured: false ## STICK into FEATURED widget
categories: ["TensorFlow", "Python"]
lang: en-US
reading_time: true
share: true
profile: true
commentable: true
math: true
---

Below we give a jupyter notebook containing the implementation of a Differentially Private Conditional GAN, originally described on Torkzadehmahani et al. 2019, with explanation of every step implemented. 

We include a TensorFlow 2 version implemented from scratch, using the Keras API and a tf.GradientTape training loop. Also to successfully use DP on a Conditional GAN, we design a custom optimizer. Experiments used the MNIST dataset.

**Pre-requisites**: (see links on notebook for suggestions of references)
- Generative Adversarial Networks (GANs)
- Differential Privacy (DP), especially DP-SGD

**We focus on the hypothetical scenario where**:
- Training data is considered sensitive.
- We aim to release a "safe" version (that does not compromise privacy) of the training data to the public.
- The goal is to allow external people to use the "safe" training data to create a classification model that performs well on the real testing data.
  - Therefore, we validate our GANs by creating models on the generated data and measuring performance.

If you intend to use any GAN with DP please consider the following notes.

**<div style='color:red'>Important notes about using DP with GANs:</div>**
- Usually the Generator is trained without DP, therefore we cannot show the data labels to the Generator. We sample labels uniformly at random on each training step.
- Although the notebook shows the one training, to report results we should train it many times from scratch and show averaged results, not maximum or single result.
- Our Validation uses the training data again to evaluate the GAN. To be 100% DP, we need to either pay some privacy budget for this step, or just use the actual generated data with cross validation for evalution.
- When generating data for creating classification models, we create the same amount of data for each label. Using the real test distribution of labels to determine the number of examples generated for each label assumes this information is public, which is rarely the case.

**Links**:
- <a target="_blank" href="https://colab.research.google.com/github/ricardocarvalhods/dpcgan/blob/master/DP_CGAN_MNIST.ipynb">Open directly on Google Colab by clicking here</a>
  - It takes 3+ hours to run the experiment completely once on Google Colab GPU
- [Github repository (with more info about method)](https://github.com/ricardocarvalhods/dpcgan)
- [Jupyter Notebook](https://github.com/ricardocarvalhods/dpcgan/blob/master/DP_CGAN_MNIST.ipynb)
