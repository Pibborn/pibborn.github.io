---
layout: page
title: Fair & Interpretable Representation Learning
description: Understandable neural networks for fair representation learning.
img: /assets/img/sellme.svg
importance: 1
category: work
---

Representation learning algorithms based on neural networks are being employed extensively in information retrieval and data mining applications.
The social impact of what the general public refers to as "AI" is now a topic of much discussion, with regulators in the EU even putting forward legal proposals which would require practitioners to "[...] minimise the risk of unfair biases embedded in the model [...]". 

The concern is that **models trained on biased data might then learn those biases**, therefore perpetuating historical discrimination against certain groups of individuals.

<div class="row">
    <div class="col-sm mt-6 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/doctor.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-6 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/scores.svg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Left: a translation model displays a gender bias. Translating English to Turkish and back shows how, when information is not sufficient, some inductive bias is needed to complete a translation task. When in doubt, the model performs the "most likely translation" by assuming that the nurse is female and the doctor is male. Right: the distribution of credit scores in the US depending on ethnicity. While credit scoring is an ethnicity-independent measurement, the difference between groups shows up as a result. Images from fairmlbook.org.
</div>

In this situation, one needs to be concerned with the fairness of a neural network, i.e. whether it is relying on sensitive, law-protected information such as ethnicity or gender to undertake its decisions. One possible approach is to remove information about the sensitive attribute from the model's internal representations. 
These technique are commonly referred to as "fair representation learning". 
These methodologies learn a projection $$f: \mathcal{X} \to \mathcal{Z}$$ into a latent space where it can be shown that the information about $s$ is minimal.

However, one issue in the area of fair representation learning is interpretability. The projection into a latent space makes it hard to investigate **why** the decisions have been undertaken. This is in open contradiction with recent EU legislation, which calls for a right to an explanation for individuals which are subject to automatic decision systems (General Data Protection Regulation (GDPR), Recital 71).

In this context, DNNs that are **fair** might still not be **transparent** enough to be applied in real-world scenarios.

Our current proposal is to employ a custom neural architecture which performs **feature corrections** for fairness.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img style="text-align:center" class="img-fluid rounded z-depth-1" src="{{ '/assets/img/sellme.svg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Instead of projecting into latent space, a possible interpretable architecture maps back onto feature space by learning a correction vector which matches in size with X. This model was trained on a US dataset dealing with law school admissions. Underpriviledged groups get a small boost to their average LSAT score so that admissions may be balanced between groups.
</div>

If you are interested in working in this topic, I have several possible avenues of research starting from this idea.

* Extending the architecture so that it may handle categorical and ordinal features naturally. 
* Limit the maximum amount of correction for each feature as a parameter which can be chosen by the user.
* Investigate the connections to the counterfactual fairness literature.

Some of the skills you will develop and knowledge you will gain by working on this topic:

* Tensorflow/Pytorch fundamentals
* Experimental tracking 
* Neural architectures for domain adaptation and fairness

Please contact me via email if interested: **mcerrato at uni dash mainz dot de**. 