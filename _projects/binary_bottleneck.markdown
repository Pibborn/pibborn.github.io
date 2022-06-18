---
layout: page
title: Binary Information Bottleneck
description: Opening the black box of deep neural networks via information.
img: /assets/img/binary.svg
importance: 2
category: work
---

The Information Bottleneck (IB) is an analysis paradigm/framework for deep neural nets (DNNs) which is rooted in Information Theory. It is rather interesting and more approachable (easier to understand) than other techniques which employ e.g. techniques from statistical mechanics. The general ideas were introduced in 1999, but from 2015 onwards they have been cast into an analysis of DNN training dynamics. This has generated a small line of papers employing this paradigm to better understand DNNs and how they work.

The mutual information (MI) between two random variables $$A$$ and $$B$$ may be defined as follows: 

$$
I(A;B) = \int_{\mathcal{A}} \int_{\mathcal{B}} p_{(A, B)}(a, b) \; log (\frac{p_{(A, B)}(a, b)}{p_A(a)p_B(b)})
$$

where $$A$$ and $$B$$ are assumed to be continuous and $p$ is the probability mass function (pmf) of the subscripted variable. $$p_{(A, B)}$$ is the joint pmf. If $$A$$ and $$B$$ are discrete, simply use summation instead of integration and the probability density function (pdf) instead of the pmf.

The core idea of the IB framework is to understand deep neural networks as functions which are **extracting relevant information from $$X$$ about $$Y$$** and to quantify their behavior via MI. Take a set of possible representations $$\mathcal{T}$$ and let $$P_{T \mid X}$$ be a transition kernel from $$\mathcal{X}$$ to $$\mathcal{T}$$. The kernel $$P_{T \mid X}$$ can be understood as a transformation of $$\mathcal{X}$$ into a representation belonging to $$\mathcal{T} \sim P_T(\cdot)$$. Then, we might write the distribution of the random variable $$T$$ as $$\int P_{T \mid X}(\cdot \mid x) \; dP_X(x)$$.


Initial work in this area has analyzed the **training dynamics** of DNNs by measuring mutual information at each epoch of training. Initial results have shown that deeper networks display faster compression of the input, i.e. $$I(X;T)$$ decreases faster during training. This is one of the first accounts of the theoretical benefits of having more layers in a deep neural network.

However, the results just mentioned above suffer from some theoretical issues. Mutual information is in general ill-defined in neural networks: if $$X$$ is a random variable representing the empirical data distribution and $$f$$ is a deterministic injective function, the mutual information $$I(X;f(X))$$ is either constant (when $$X$$ is discrete) or infinite (when $$X$$ is continuous) \cite{goldfeld2019estimating}.
As activation functions in neural networks such as sigmoid and htan are injective and real-valued, $$I(\tell; S)$$ is infinite. When the ReLU activation function is employed, the mutual information is finite but still vacuous.

To solve this issue, we have developed a neural architecture which employs **stochastic quantization** as a way to generate random representations. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/binary.svg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    A stochastically quantized neural network.
</div>

I am looking for students who are interested in better understanding deep neural network to contribute to this project. We have developed a solid theory of how to employ our stochastically quantized networks to explore the IB problem and we are now looking to perform experiments in this area.

Interested students may contact me via email: **mcerrato at uni dash mainz dot de**.
