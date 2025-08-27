---
layout:     post
title:      "A Year of Being an AI Startup Founder"
date:       2025-08-25 20:15:00
summary:    "Thoughts on the generative AI boom and what will become of the industry"
tags:       ai ethics
---

In June 2024, I co-founded a startup and served as the CTO. Our mission was to build products to bring LLM-based tech orgs up the maturity curve. We initially started in cybersecurity but pivoted our product to evaluations, fine-tuning, model comparisons, and other problems that turned out to be more pressing for our customers. We wound down operations in July 2025.

This blog post is a summation of my thoughts from the previous year, and my predictions about the AI industry.

## tl;dr

* The AI bubble is deflating right now in summer 2025.
* Consumer access of ChatGPT is at best net neutral, if not a net negative to society.
* API access is a net positive only for enterprises that use it with maturity and strong investment in evaluations, process, and cybersecurity. Even code auto-complete should be used with care, let alone coding agents and customer-facing products.
* Creative fields have not figured out a good use for LLM and image generation technology, and maybe never will due to the fundamental nature of these models.

## The AI Bubble

### Unit economics

It costs an LLM provider like OpenAI billions of dollars to train a new model. Each new model requires more compute, which means newer GPUs and bigger data centers. This costs a lot of money. In theory, they should be able to cover this cost with the profit on their consumer business and their API business. However, Sam Altman has recently admitted to only, at best, breaking even on every inference made. The unit economics is not adding up and is certainly not pointing to the massive valuations these LLM providers are getting from investors.

Even companies like MS, Google, and Meta are funding their generative AI divisions using revenue from their other business units.

Valuations are based on vibes. Public backlash as well as the CEOs themselves pumping the breaks on their own hype is shifting the vibes. Satya Nadella off-handedly mentioned that LLM CEOs get on a weekly group call, essentially working as a cartel in terms of setting the tone of the industry. They've wisened up to the fact that they can no longer sustain the hype required to support their valuations. The bungled release of GPT-5 and the disappointment their users felt has been the tipping point. The vibes are undeniably shifting.

### Public sentiment

As more people experience ChatGPT, the more people over-hype and over-rely on LLMs. This leads to a larger number of people who come into contact with these bad actors, permanently and negatively affecting their viewpoint on consumer LLM technology.

Let's say you work with someone who you need help from. You message them on Slack asking them a question. Their 3-paragraph reply begins in perfect LLM tone: "Certainly, I can help you with that!" You get pissed off and feel betrayed. You come away from this interaction associating this annoying coworker with LLMs. You vow never to touch ChatGPT.

I've heard this story from friends, family, and strangers on the internet a couple dozen times in the last few months.

## ChatGPT considered harmful

This next point is related to the previous one.

The AI-hype in the news media is giving way to an increasing number of horror stories: people lured by chatbots to injury or death, psychosis caused by agreeable LLMs keeping vulnerable people trapped in negative thought loops, even a teenager committing suicide after an LLM explicitly encouraged him to.

When an LLM is used in an enterprise context, guardrails against these cases are unimportant. If a software engineer integrates with the Anthropic API to extract phone numbers from PDFs, then there doesn't need to be a bullet point in the system prompt telling the LLM to refrain from giving answers that may harm someone.

## Enterprise use cases

1. Tech orgs are not prepared for the cybersecurity risk of LLM
2. Tech orgs need to continuously evaluate their LLM output quality in production, regardless of whether it's internal tooling or customer-facing products
3. It's also a change management issue because teams need processes in place to get the subject matter experts to be in touch with what their LLMs are doing. LLMs become their surrogate in these situations and there needs to be a direct chain of responsibility from the LLM to its owners.

Diffusing the responsibility of the LLM into the organization at large leads to perverse incentives. LLMs become a way to do stupid things faster. If there is no individual responsible for its outputs, it can diverge from intentions quickly, even as soon as it gets deployed.

## Using LLMs for creation

> AI is fake and it sucks.

This is a phrase I've heard many times and honestly, in this context, it's actually getting to a truth many people don't want to admit.

What is the purpose of art? It's a way for a human being to reach across space and time, maybe centuries, to touch another human being. When an LLM or image model produces a string of text or a rectangle of pixels, at it's most ideal form, it's curated by a human being in order to transmit a copy to produce a few microliters of dopamine in someone else's brain. At its center, there's a hollowness that reveals a lot about how little creative work is valued.

People like to bring up that David Lynch, shortly before his death, told Natasha Lyonne that AI is a tool, like a pencil, and it can be used for good. First off, she is an unreliable narrator in this case, and secondly, there's not much context around what he meant. Plus, even a respected artist can be wrong when making a grand statement like this. I think he could be right but only in a specific context.

Oblique strategy cards and random number generators are two analogous technologies that can be helpful to an artist. Yes, you can roll a set of dice to decide what key to write your song in. Yes, you can [use procedural generation](https://samplereality.com/2025/07/18/the-poetics-and-power-of-small-language-models/) to create an artwork. But creating a novel or a digital painting from a statistical model is at best a novelty, not something that fulfills the fundamental need for art in a human soul.

## Ethics

I'm not a moral philosopher but I'd like to talk about the ethics of all of this.

LLMs are trained on public domain data as well as whatever text and images that LLM provider companies can get their hands on. It's a shredded up version of all recorded history, other nonfiction, fiction, and everything in between. Many of the living creators of these works have expressed that they don't want their works used in this way. The legality of LLM providers training models from these works is still being settled with lawsuits moving through the US justice system. But ethically, every inference you make using an LLM is against the wishes of many people whose works directly power it. It's something for you to consider before you use it.

The SF Bay Area rationalist community generally subscribes to utilitarian ethics and the allure of "number go up" is certainly strong. But that doesn't mean all other systems are invalid somehow. A large portion of ethics and moral philosophy professors support other systems such as virtue ethics. Even if you believe that the majority of people have had their lives improved by LLMs, consider the possibility that it's a harmful technology along another axis that a lot of people in the field of ethics care about.