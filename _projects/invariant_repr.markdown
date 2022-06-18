---
layout: page
title: Invariant representation learning
description: Removing symbols from sub-symbolic representations.
img: /assets/img/adv-net.png
importance: 3
category: work
---

Representation learning algorithms based on neural networks are being employed extensively in information retrieval and data mining applications.
The social impact of what the general public refers to as "AI" is now a topic of much discussion, with regulators in the EU even putting forward legal proposals which would require practitioners to "[...] minimise the risk of unfair biases embedded in the model [...]". 

The concern is that **models trained on biased data might then learn those biases**, therefore perpetuating historical discrimination against certain groups of individuals.

While it is of course possible to avoid training our ML models on sensitive data such as gender or ethnicity, other features contained in the data may constitute a "proxy" for sensitive information. Consider, as a simplified example, a ML model assigning loans to people. A very important feature in this setting would be the credit score of an individual. A higher credit score represents a higher probability for solvency. Due to the economic disparities across ethnical groups, however, this feature also constitutes a strong proxy for ethnicity.

<div class="row">
    <div class="col-sm mt-6 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/scores.svg' | relative_url }}" alt="" title="Credit scores in the US."/>
    </div>
</div>
<div class="caption">
    The distribution of credit scores in the US depending on ethnicity. While credit scoring is an ethnicity-independent measurement, the difference between groups shows up as a result. Image from fairmlbook.org.
</div>

In the Adult dataset, for instance, it is possible to predict an individual's gender with good accuracy from the remaining available features. Fair representation learning employs neural networks to remove information about such sensitive data. 

<div class="row">
    <div class="col-sm mt-6 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/adv-net.png' | relative_url }}" alt="" title="An adversarial learner"/>
    </div>
</div>
<div class="caption">
    An example fair representation learning algorithm. 
</div>

Performance estimations in fair representation learning usually employ the learned, "fair" features to predict the sensitive information which was removed. When the classifier mostly fails in doing so, we say that our algorithm is working. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img style="text-align:center" class="img-fluid rounded z-depth-1" src="{{ '/assets/img/adult-performance.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Performance of various fair representation algorithms in removing information about gender on the Adult dataset. Closer to the dotted line is better.
</div>

My interest is in this area is to perform a large-scale study of fair representation learning algorithm to test them rigorously on this idea and comparing them to simpler baselines. Information theory tells us that we should not be able to remove information from representations; nonetheless, fair representation algorithms are still researched broadly. 

As a way to further the academic discussion on this matter, we intend to release a large database of "fair representations" which may then be investigated by other research groups. 

Some of the skills you will develop and knowledge you will gain by working on this topic:

* Tensorflow/Pytorch fundamentals
* Experimental tracking 
* Neural architectures for domain adaptation and fairness
* Open science and reproducibility

Please contact me via email if interested: **mcerrato at uni dash mainz dot de**. 