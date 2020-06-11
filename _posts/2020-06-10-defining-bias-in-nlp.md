---
layout:     post
title:      "What does it mean for a machine learning system to be biased?"
date:       2020-06-10 23:09:00
summary:    "Language (Technology) is Power: A Critical Survey of Bias in NLP"
tags:       machine-learning ethics ai
---

I recently read this paper: [Language (Technology) is Power: A Critical Survey of "Bias" in NLP](https://arxiv.org/abs/2005.14050)

Its basic conclusion is that the Natural Language Processing field has not settled on a rigorous definition of bias yet. By analyzing 146 NLP papers that attempt to measure or address bias, the authors discover that the field has settled on a handful of related definitions. Each one is valid and worthy of addressing by itself, but it would be impossible to attack these problems all at once.

This survey categorizes bias in NLP literature into the following groups:

* Representational harms. Usually manifested as stereotyping.
* Allocational harms. Usually the harms caused by systems downstream from those that cause representational harms.
* Questionable correlations. Systems that behave differently based on language features associated with particular social groups.

The authors suggest that the issue of deinfing bias in NLP systems more clearly would become easier if researchers started doing the following:

* Cite work outside of the NLP or machine learning field when talking about bias. There's plenty of work already analyzing the relationship between language use and social hierarchies. Use these at least in the motivation section of your paper.
* Stop shying away from directly discussing why the particular brand of bias your work is tackling is harmful, and to whom. Nailing down the definition of something as vague as bias will be impossible unless we talk about who exactly will be affected by it.
* Study and place value on the lived experiences of the communities that will be affected by NLP systems. Stop focusing so much on incremental improvements to existing systems (new debiased datasets, new language models) and start questioning the relationship between technologists, technologies, and the communities directly affected.

This paper suggests a massive shift in the way most of the [FATML](https://www.fatml.org/) crowd has approached these issues so far. It encapsulates a lot of the concerns I've had with the work I've seen in FATML: an overabundance of focus on incremental updates to something like a word embedding model, and not enouch work like [this one from 2018.](https://arxiv.org/pdf/1807.00553.pdf)

I believe this work is extremely important and increasingly urgent. Without rigorous thought about ethics in NLP, we're heading into a new phase in the information age with a scary amount of naïveté.