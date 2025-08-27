---
layout:     post
title:      "A Year of Being an AI Startup Founder"
date:       2025-08-25 20:15:00
summary:    "Thoughts on the generative AI boom and what will become of the industry"
tags:       ai ethics
---

In June 2024, I co-founded a startup and served as the CTO. Our mission was to bring LLM-based tech orgs up the maturity curve. We initially started in cybersecurity but pivoted our product to evaluations, fine-tuning, model comparisons, and other problems that turned out to be more pressing for our customers. Even though we raised pre-seed funding and won some customers, we made the hard decision to wind down operations in summer 2025.

This blog post is a summation of my thoughts and learnings from the previous year and my predictions about the AI industry.

## tl;dr

* The AI bubble is deflating right now in summer 2025.
* Consumer access of ChatGPT is at best net neutral, if not a net negative to society. We are unprepared to handle what it's doing to us.
* API access to LLMs is a net positive only for enterprises that use it with maturity and strong investment in evaluations, process, and cybersecurity. Even code auto-complete should be used with care, let alone coding agents and customer-facing products.
* Creative fields have not figured out a good use for LLM and image generation technology, and maybe never will due to the fundamental nature of these models.

## The AI bubble is deflating

### Unit economics

It costs an LLM provider like OpenAI billions of dollars to train a new model. Each new model requires more compute, which means newer GPUs and bigger data centers. This costs a lot of money. In theory, they should be able to cover this cost with the profit on their consumer business and their API business. However, OpenAI CEO Sam Altman has recently admitted to only, at best, breaking even on every inference made. [The unit economics is not adding up](https://www.wheresyoured.at/how-to-argue-with-an-ai-booster/#ultimate-booster-quip-the-cost-of-inference-is-coming-down-this-proves-that-things-are-getting-cheaper) and is certainly not pointing to the massive valuations these LLM providers are getting from investors.

Even companies like MS, Google, and Meta are funding their generative AI divisions using revenue from their other business units.

Valuations are based on vibes. Public backlash as well as the CEOs themselves [pumping the breaks on their own hype](https://arstechnica.com/information-technology/2025/08/sam-altman-calls-ai-a-bubble-while-seeking-500b-valuation-for-openai/) is shifting the vibes. They've wisened up to the fact that they can no longer sustain the hype required to support their valuations. The bungled release of GPT-5 and the disappointment their users felt has been the tipping point. The vibes are undeniably shifting.

I will concede that the use of generative AI is rising in various industries [according to this March 2025 McKinsey report.](https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai) But the report also says:

> Yet gen AI’s reported effects on bottom-line impact are not yet material at the enterprise-wide level. More than 80 percent of respondents say their organizations aren’t seeing a tangible impact on enterprise-level EBIT from their use of gen AI. Organizations have been experimenting with gen AI tools. Use continues to surge, but from a value capture standpoint, these are still early days—few are experiencing meaningful bottom-line impacts.

So this is a technology that's been pushed on the workforce for 2 years and we're just not seeing the benefits they'd predicted we would see. When should we call it a bust? 1 more year of this? 2 more years?

### Public sentiment

As more people experience ChatGPT, the more people over-hype and over-rely on LLMs to the point of being annoying. This leads to a larger number of people who come into contact with these bad actors, permanently and negatively affecting their viewpoint on consumer LLM technology.

Let's say you work with someone and you ask them for help on a topic. You message them on Slack asking them a question. Their 3-paragraph reply begins in perfect LLM tone: "Certainly, I can help you with that!" You get pissed off and feel betrayed because they couldn't take the time to talk to you, and instead did the modern equivalent of [lmgtfy](https://letmegooglethat.com/). You come away from this interaction associating this annoying coworker with LLMs. You vow never to touch ChatGPT and in fact you think it makes the world a worse place.

I've heard this story from friends and family a couple dozen times in the last few months. Anecdata, yes, but it's a repeating pattern that's worth taking seriously if you think LLMs are the future of work.

## ChatGPT considered harmful

This next point is related to the previous one.

The AI-hype in the news media is giving way to an increasing number of horror stories: people lured by chatbots to injury or death, psychosis caused by agreeable LLMs keeping vulnerable people trapped in negative thought loops, even a teenager committing suicide after an LLM explicitly encouraged him to.

When an LLM is used in an enterprise context, guardrails against these cases are unimportant. If a software engineer integrates with the Anthropic API to extract phone numbers from PDFs, then there doesn't need to be a bullet point in the system prompt telling the LLM to refrain from giving answers that may harm someone.

I believe that the free tier of ChatGPT is eroding some of the basic functions of society. By introducing synthetic interactions into everyday life, the side-effects of real organic interactions get sanded away, leaving behind some strange hypernormal stimulus that our society and our brains are ill-equipped to handle.

Let's be real: LLMs are not substitutes for people. It's not like autocomplete, it's not like an intern, and it's not like a therapist. It's something else entirely. Most of us don't have the mental model to be able to hold these ideas in tension every time we "talk" to ChatGPT. In fact, we aren't actually talking to anything! See? We don't even have the right words to describe what's happening when a user interacts with an LLM. Let alone the capability to correctly slot it into the exact right gap in our lives.

## Enterprise use cases

1. Tech orgs are not prepared for the cybersecurity risk of LLMs. LLMs are fundamentally insecure pieces of technology both due to their stochasticity and the fact that [their structure prevents them from differentiating between trusted and untrusted input token streams.](https://simonwillison.net/2025/Aug/25/agentic-browser-security/)
2. Tech orgs need to continuously evaluate their LLM output quality in production, regardless of whether it's internal tooling or customer-facing products. To neglect this is malpractice.
3. Integrating LLMs into a team is a change management issue because teams need processes in place to get the subject matter experts to be directly responsible for what their LLMs are doing. This involves regular manual evaluations of output samples and error analysis. Internal tooling (either built or bought) can reduce friction, but at the end of the day, subject matter experts must be incentivized to do the tedious work of finding issues and correcting them.

Diffusing the responsibility of the LLM into the organization at large leads to perverse incentives. LLMs become a way to do stupid things faster. If there is no individual responsible for an LLM's outputs, it can diverge from intentions quickly, even as soon as it gets deployed.

Quoting the [March 2025 McKinsey report](https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai) I linked above:

> So far, less than one-third of respondents report that their organizations are following most of the 12 adoption and scaling practices, with less than one in five saying their organizations are tracking KPIs for gen AI solutions.

[There is no silver bullet](https://web.archive.org/web/20160910002130/http://worrydream.com/refs/Brooks-NoSilverBullet.pdf) but it's really tempting for tech leaders to pretend like LLMs are one. Whether it's copilots for writing code or customer service chatbots, it's hard to resist simply dropping in an LLM-based solution and hoping for the best. What seem like common sense measures, because they may be a little challenging to implement, are often ignored for the sake of product velocity. I believe this will come back to bite tech orgs in the near future.

## Using LLMs for creation

> AI is fake and it sucks.

This is a phrase I've heard many times and honestly, in the context of creative work, it's actually getting to a truth many people in the LLM world don't want to admit.

What is the purpose of art? It's a way for a human being to reach across space and time, maybe centuries, to touch another human being. When an LLM or image model produces a string of text or a rectangle of pixels, at it's most ideal form, it's curated by a human being in order to transmit a copy to produce a few microliters of dopamine in someone else's brain. At its center, there's a hollowness that reveals a lot about how little creative work is valued.

People like to bring up that director and artist David Lynch, shortly before his death, [told actor and writer Natasha Lyonne](https://www.forbes.com/sites/danidiplacido/2025/06/05/natasha-lyonne-sparks-backlash-after-quoting-david-lynch/) that AI is a tool, like a pencil, and it can be used for good. First off, she is an unreliable narrator in this case, and secondly, there's not much context around what he meant by that. I think he could be right but only in a specific context.

Oblique strategy cards and random number generators are two analogous technologies that can be helpful to an artist. You can roll a set of dice to decide what key to write your song in. You can [use procedural generation](https://samplereality.com/2025/07/18/the-poetics-and-power-of-small-language-models/) to create art. These are tools in the creative process that allows an artist to unblock themselves and create something that's a more complete expression of what they want to express. But creating a novel or a digital painting from a statistical model is at best a novelty, not something that fulfills the aim of art in human society.

## Ethics

I'm not a moral philosopher but I'd like to talk about the ethics of generative AI.

LLMs are trained on public domain data as well as whatever text and images that LLM provider companies can get their hands on. It's a shredded up version of all recorded history, other nonfiction, fiction, and everything in between. The training data is the blood, sweat, and tears of thousands of creators.

[Many of the living creators of these works have expressed that they don't want their works used in this way.](https://arstechnica.com/tech-policy/2025/08/authors-celebrate-historic-settlement-coming-soon-in-anthropic-class-action/) The legality of LLM providers training models from these works is still being settled with [lawsuits moving through the US justice system.](https://sustainabletechpartner.com/topics/ai/generative-ai-lawsuit-timeline/) But ethically, every inference you make using an LLM is against the wishes of many people whose works directly power it. It's something for you to consider before you use it.

The SF Bay Area rationalist community, whose philosophy strongly influences the tech CEOs in charge of this industry, generally subscribes to [consequentialist ethics](https://plato.stanford.edu/entries/consequentialism/). They hold the belief that LLMs help people more than they harm people. The allure of utilitarianism's "number go up" reasoning is certainly strong. But that doesn't mean all other systems of ethics are invalid. A large portion of ethics and moral philosophy professors support other systems such as virtue ethics. Even if you believe that the majority of people have had their lives improved by LLMs, consider the possibility that it's a harmful technology along another axis that a lot of people in the field of ethics care about.

### Electricity and water use

Many skeptics bring up the power use and water use of training and inference of LLMs. I haven't seen compelling evidence that it's substantially increasing greenhouse gases or taking water away from communities. The news articles and opinion pieces I've seen have not made the case strongly enough for me to abstain from LLMs for those specific reasons.

[Here's an article that makes a good faith effort to show that LLM and image generation usage at current levels isn't something to be freaked out about.](https://andymasley.substack.com/p/a-cheat-sheet-for-conversations-about) Video generation, on the other hand, is to be avoided because it requires orders of magnitude more energy.

What gives me pause, however, is the amount of investment that cloud providers are putting into building new data centers. As these data centers come online, we may see these ill effects. This, in conjunction with every Google search making LLM inferences, are causes for concern about rises in energy consumption in the near future. I am hopeful, however, this will cause second-order effects that incentivize building small modular nuclear reactors or other clean energy investments like wind and solar.

## Overall thoughts

I believe LLM usage will come to an equilibrium soon. It's a powerful technology if integrated in the right way. The C-suites that force their workers to use LLMs are buying into hype and may be driving teams to use LLMs irresponsbily. Consumer usage of ChatGPT, Claude, and other free-tier LLMs are probably harmful to society in the long run. The LLM industry will see a market correction soon that I hope will set some of these things right.