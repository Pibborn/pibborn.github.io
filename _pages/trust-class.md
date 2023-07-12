---
layout: page
permalink: /trust-class/
title: Trustworthy AI - Fairness, Interpretability and Privacy
description: 
nav: true
---

Machine Learning models, especially based on neural networks, are now part of our everyday life, being deployed in smartphones and embedded systems. Computer Vision algorithms recognize our pets in the photos we take; Natural Language Processing models are able to fix our grammar and even generate human-passing text. 

While the new wave of so-called "deep learning" systems displays impressive performance in various tasks, these models are very hard to understand in various ways. To cite one issue among others, the GPT family of models employs 175 billion learnable parameters. When something goes wrong, it is almost impossible to understand "why" a model has made a particular decision.

The technical optimism and excitement around Machine Learning has also pushed businesses to apply it in situations where it may impact people's well-being directly, such as loan applications, candidate selection for job offers and evaluating the chance of re-offending for people who commited crimes. Computer vision applications based on neural networks have even been employed to judge beauty contests.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/beauty.png' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/guardian_small.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/forbes.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    When we do not fully understand AI algorithms, consequences of their application are hard to predict.
</div>


In such contexts, opaque models are particularly problematic as there is a concrete risk for discrimination against certain groups of people. Protected characteristics such as gender and ethnicity might be used in the computation of the final decision, which is problematic on moral grounds and unlawful. The existence of the gender pay gap, for example, shows how there are complex correlations between law-protected attributes (gender) and other, non-sensitive attributes such as a person's yearly salary.

If models are learning from biased data, it follows that they will learn to output biased decisions; if we are unable to explain those decisions, we are left with very little human control over what ultimately is a software process. On top of being philosophically troubling and unethical, recent legislation might see these methodologies as unlawful. Taking the General Data Protection Regulation in the European Union as an example, transparency and fairness have to be guaranteed to individuals who are subject to automatic decision-making software systems.

<hr>

During this class, you will learn about the current discussion in the AI and ML literature about how to control AI and ML algorithms so that they are trustworthy. We will be focusing on three characteristics especially:

* Fairness: how can we learn non-discriminating models from biased data?
* Interpretability: how can we make sense of a model's decisions?
* Privacy: how do we make sure that a model trained with our personal data does not leak our data to third parties?

The class is taught on **Tuesdays 10-12AM** in Room **04-426**. We will also have tutorials - date and time TBD. 

<hr>

Class Schedule (official) and topics (tentative):

| Lecture 	|         Date         	|   From  	|    To   	|   Room  	|                     Topic                    	|                                                                   Recommended Reading (before class)                                                                   	|
|:-------:	|:--------------------:	|:-------:	|:-------:	|:-------:	|:--------------------------------------------:	|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------:	|
|    1    	| Tue, 24. Oct. 2022   	| 10:00   	| 12:00   	| 04 426  	|                 Introduction                 	| Stanford Encyclopedia of Philosophy: [AI](https://plato.stanford.edu/entries/artificial-intelligence/), [Ethics of AI](https://plato.stanford.edu/entries/ethics-ai)   	|
|    2    	|  Tue, 7. Nov. 2022   	| 10:00   	| 12:00   	| 04 426  	| Machine Learning and Probabilistic Inference 	|                                                                                                                                                                        	|
|    3    	| Tue, 14. Nov. 2022   	| 10:00   	| 12:00   	| 04 426  	|      Bias in Measurement, Bias in Models     	|  |
|    4    	| Tue, 14. Nov. 2022   	| 10:00   	| 12:00   	| 04 426  	|      Fairness and Egalitarianism                               |
|    5    	| Tue, 21. Nov. 2022   	| 10:00   	| 12:00   	| 04 426  	|          Fair preprocessing of data          	|                                                                                                                                                                        	|
|    6    	| Tue, 28. Nov. 2022   	| 10:00   	| 12:00   	| 04 426  	|           Regularization Approaches          	|                                                                                                                                                                        	|
|    7    	|  Tue, 5. Dec. 2022   	| 10:00   	| 12:00   	| 04 426  	|         Learning Fair Representations        	|                                                                                                                                                                        	|
|    8    	| Tue, 12. Dec. 2022   	| 10:00   	| 12:00   	| 04 426  	|     Explaining ML: Post-Hoc Explanations     	|                                                                                                                                                                        	|
|    9    	| Tue, 19. Dec. 2022   	| 10:00   	| 12:00   	| 04 426  	|     Interpreting ML: Glassbox models  	|                                                                                                                                                                        	|
|    10    	| Tue, 9. Jan. 2023   	| 10:00   	| 12:00   	| 04 426  	|             Differential Privacy: Introduction            	|                                                                                                                                                                        	|
|    11   	| Tue, 16. Jan. 2023   	| 10:00   	| 12:00   	| 04 426  	|                      Differential Privacy: Laplace and Gaussian Mechanisms                    	|                                                                                                                                                                        	|
|    12   	| Tue, 23. Jan. 2023   	| 10:00   	| 12:00   	| 04 426  	|                      Differentially-private Machine Learning                     	|                                                                                                                                                                        	|
|    13   	| Tue, 30. Jan. 2023   	| 10:00   	| 12:00   	| 04 426  	|                      Review Session                     	|                                                                                                                                                                        	|
