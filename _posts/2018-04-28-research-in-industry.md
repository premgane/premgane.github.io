---
layout:     post
title:      Doing Research in the Industry
date:       2018-04-28 15:46:00
summary:    "Similarities and differences between academia and the industry"
categories: research
---

In my career, I’ve worked in several research settings. In undergrad and during my Masters, I worked in research Natural Language Processing labs. I was a research assistant, so my tasks revolved around data gathering & cleaning, analysis, and annotation. I also did some software engineering and sysadmin work to run experiments.

While I never led a research team in academia, I have been given this opportunity in my current position as Lead NLP Engineer at Agolo, a small startup in NYC. From this perspective, I’ve noticed several differences between doing research in academia and in the industry.

I’ll attempt to lay out my observations in this post without an editorial bias. I’ll save my overall opinions for the conclusion section.

Please keep in mind this post is not meant to be authoritative. I have much more experience working in the industry than I do working in an academic research lab.

## Differences
Research projects in academia are obviously different from projects in the industry, all else being equal. Even the exact same project will have different outcomes depending on what kind of team conducts the research. The university lab looks for opportunities to publish the work, while the startup has the pressure to convert the research output into a production-ready system.

However, the differences in goals go a little deeper than just the end outcome. These divergent goals have profound effects on several aspects of the project:

* How the deadlines are structured
* How the project’s milestones are designed
* Which projects get picked in the first place
* The definition of a successful or unsuccessful project

### Deadlines and milestones
The publication deadlines of major conferences have a huge impact on the way academic research is conducted. A PhD student’s thesis is broken down into smaller projects, each of which should become a paper.

On the other hand, in the industry, deadlines are set either by major clients or major product milestones. The research project is organized by  what the end-user is expecting, and the results need to be in line with customer expectations. If it is to become a piece of software running in production, it would most likely follow Agile software practices and release early and often.

This brings us to the next point:

### Choice of projects
In an academic setting, projects are chosen based on a different set of criteria than in an industrial setting. The amount of grants available in a certain line of research, the overall interests of the research lab, and the research interests of the principal investigator are some of the main concerns of a research lab. None of these are relevant to industrial research.

In the industry, a tight feedback loop between the customer and the researchers inform the projects being done in the research team. The customer, particularly in a well-focused startup, is the primary motivation for almost any industrial research undertaking. To that end, the research team will need to be in touch with other functions of the startup: engineering, product, and sales. Ideally, the research team would also be in contact with end users and clients, too.

To be clear, this does not imply that the industrial research team needs to only work on short-term investigations or products the customer directly requests. The user-focused point of view will actually inform the research team’s long-term projects and research goals as well. In both cases, the important thing is to start from the user and work backwards.

### Acceptable results
In an academic setting, a line of research is considered viable if it makes a statistically significant improvement over existing approaches and baselines. Alternatively, a novel approach to an existing problem, a statement of a new problem & metrics, or the release of a new dataset might all be desirable results. These results are reasonably publishable.

In the industry, because of the user-focused approach, many of these results may not be sufficient. They could be milestones in a larger project, but the definition-of-done is based on the user. The quality and speed of the resulting system are held to different standards than in academia.

For example, a real-time system with high precision but very low recall may be acceptable to a startup, as long as it’s well-architected, maintainable, and scalable. On the other hand, an academic lab may need to publish a high-F1-scoring model even though it works in a batch processing way and takes several days to run.

In the industry, the requirements of the product have a large effect on the compromises that will have to be made. In academia, the quantitative result on a known benchmark is often the main aspect that matters.

Frequently, an industrial research team may find improvements over baselines, or at least, over what is currently implemented in production. However, if it does not make a noticeable difference in the product, it is unlikely to be pursued further.

This is especially true in smaller startups, where resource constraints are a real issue day-to-day. The size of the team and the available budget will hinder the further pursuit of lines of research that may be promising candidates for papers. However, for a slightly larger team, this might be a viable approach to get a white paper published.


## Similarities
While this post focuses on the differences, I’d also like to point out some similarities between academic and industrial research.

In both settings, the research team has to balance priorities of short-term and long-term projects. The short-term projects need to lead up to a long-term goal.

In the industry, the long-term goal may be quarterly or annual results. The metrics and features that the company is trying to achieve are translated into the long-term research goals, which then break down into short-term projects. In the short-term, vying for attention are the smaller enhancements and features that need to get done in order to satisfy customer asks.

Another similarity is in team dynamics and management. The vision of the research team needs to be communicated clearly and internalized by individual contributors regardless of the setting. Research requires care, attention to detail, and a drive to improve what exists. This level of commitment and collaboration can only happen when each team member is aligned on a strong vision and sets aside their ego.


## Conclusion
Personally, I like working in the industry. I have a software engineering background, so working backward from the customer seems like a natural approach. I like maintaining a balance of research tasks and engineering tasks, and I get to incorporate my interests in software architecture as well.

In my opinion, every researcher needs to try working in both of these environments to choose what works for them personally. They also need to recognize that their preferences may change over time. Neither one is a clear winner, objectively speaking. They are both important in different ways.









