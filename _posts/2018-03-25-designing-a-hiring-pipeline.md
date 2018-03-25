---
layout:     post
title:      Designing a Hiring Pipeline at a Startup
date:       2018-03-25 11:20:00
summary:    "The best practices at a large company may not work at a small-sized startup"
categories: startups hiring
---

When hiring for an engineering position, most people would turn to the internet to get up to date on the latest best practices. Most of the guidelines and advice on the internet comes from large companies, so their advice is aimed at similarly large organizations.

For example, the hiring process at a big-name software company might be a full day of five or six whiteboard coding interviews with a lunch break in the middle. Afterwards, the hiring committee would meet to vote on whether the candidate passed the hiring bar.

In the case of a startup with fewer than 15 employees total, some of whom are non-technical folks, this hiring process does not work. We simply don't have enough engineers to do all-day interviews. Even if we did, engineers would spend a disporportionate amount of time interviewing and not working on our technical tasks.

So, what can we do? How do we design a pipeline to spend the least amount of time interviewing? How do we write questions that can give us the clearest picture of the candidate? How do we enable the candidate to reveal enough about their skills that we can accurately imagine what it would be like to work with them?

I was recently tasked with designing the hiring process for NLP Engineer at Agolo, my place of work. I set out to find the latest and greatest ideas in hiring practices to design a process that is fair, effective, and efficient.

After some research, I came up with the following guidelines.

## General principles

1. The interviews should only cover what the candidate will directly apply in the role if they are hired. For instance, we should not use logic puzzles as a proxy to measure problem-solving abilities. For more details, [please see this interview with Laszlo Bock, an SVP at Google.](http://www.nytimes.com/2013/06/20/business/in-head-hunting-big-data-may-not-be-such-a-big-deal.html?pagewanted=all)
1. The interviews should allow the candidate to reveal a breadth of knowledge and an understanding of deeper nuances.
1. The candidate will need to have technical and non-technical skills regardless of how technical the role is.

We distilled these principles down to three types of questions: breadth questions, depth questions, and non-technical questions.

Let's take a look at each one.

## Breadth questions

Breadth questions, ideally, should be short but numerous. By testing breadth, we are trying to ensure that the candidate has no glaring holes in knowledge. Even though the candidate may not be an expert in everything, they should be able to contribute at a basic level to solving problems in multiple related areas.

We took inspiration from [this classic Steve Yegge blog post.](https://sites.google.com/site/steveyegge2/five-essential-phone-screen-questions) From that post:

> Please understand:   what I'm looking for here is a total vacuum in one of these areas. It's OK if they struggle a little and then figure it out. It's OK if they need some minor hints or prompting. I don't mind if they're rusty or slow. What you're looking for is candidates who are utterly clueless, or horribly confused, about the area in question.

Depending on the role, we may not want to test the specific areas that Yegge outlines in his post. However, the idea behind the Breadth questions is the same -- we are asking ourselves, "will this candidate be completely lost if presented with a problem slightly outside of their specialization?"

For example, for our research scientist roles, we want candidates who can code quickly as well as think on their feet to solve research problems. So, we would give them several 5-minute coding problems and a few 5-minute research problems to discuss.

We would write these questions by simplifying real-world problems we have solved in the past. The goal is to cover as many areas as possible with these questions. We want to see how the candidate approaches these problems, gauge their level of comfort with each topic, and test their instincts. We can learn a surprising amount about a candidate's abilities by looking at their initial response to a problem.

## Depth questions

Testing for depth of knowledge is tricky because we only have a limited amount of time to talk to the candidate.

The best ways to test whether the candidate has depth of knowledge are:

1. asking them to explain a complex concept in simple terms, or
2. solve a difficult problem that uses the concept.

[Explaining complicated concepts in simple terms is a good measure of understanding.](https://kottke.org/17/06/if-you-cant-explain-something-in-simple-terms-you-dont-understand-it)

If the candidate can solve a complicated real-world problem in a short period of time while explaining it, then even better.

Our depth questions are designed to mimic as faithfully as possible the real problems the candidate would solve day-to-day if hired. The candidate for the NLP Engineer role would not only plan, scope, and execute experiments end-to-end, but also work on wrangling noisy data, presenting results, and productizing the system by working alongside software engineers.

We want to test whether the candidate is adept at all parts of the plan-execute-refine cycle of bringing an experimental approach to production. When solving these real-world questions, the interviewer tries to imagine what it would be like to work with the candidate every day. By removing the pretenses of interviewing as much as possible, the interviewer can get valuable insights into:

1. the way the candidate approaches a problem,
1. how well they can design experiments and estimate the time and effort needed, and 
1. whether the candidate can anticipate multiple outcomes at each step of the plan.

Each of our depth questions may take 20 minutes to solve. They allow us to keep digging deeper to simulate the process of working on a project, start to finish. They also simulate a real brainstorming and project-planning meeting that the candidate would lead if they were hired. These deep-dive questions allow the interviewer to more accurately imagine what it would be like to work with this candidate on complicated projects.

## Non-technical questions

Regardless of how technical the position, nobody at a startup works in a vacuum. The interview process should test as deeply as possible the ability of the candidate to accomplish the following:

1. discuss deeply technical concepts in semi-technical language
1. collaborate within a team comprised of members of varying technical skills, staying level-headed to work through conflicting opinions
1. speak thoughtfully about a wide ranging set of topics, including the societal impact of the industry
1. demonstrate an ability to objectively analyze their own strengths and limitations

We have found that the best way to test these skills is to isolate some non-technical questions into its own interview. For this interview, we use interviewers who aren't fully familiar with the concepts within the candidate's expertise. In a small startup, the candidate would be working closely with team members of varying backgrounds, so it's crucial that we see how well they can adapt their communication style.

## Other practical considerations

These are some other guidelines that we have found useful in designing our pipeline:

### Kindness and empathy

We should support the candidate and enable them to succeed as much as possible. The candidate and the interviewer are on the same team because they both want the position to be filled by someone who is a good fit. Furthermore, the interviewer is representing the company, and the candidate should walk away with a good feeling about the company regardless of how well they did in the interview. Kindness is key.

### Inclusivity in hiring

Those who are designing the interviews should put effort into making the process as inclusive as possible. By neglecting inclusivity, we are unconsciously eliminating entire groups of people from being able to pass our interviews, even though many qualified individuals in those groups may be a good fit for the role. This is bad for the company and bad for those who are often excluded.

These are some articles and blog posts that I found useful to get me started thinking about this: [1](https://work.qz.com/1095637/diversity-and-inclusion-a-guide-to-unbiased-hiring-from-quartz-at-work/), [2](https://www.ziprecruiter.com/blog/the-right-way-to-incorporate-diversity-hiring-goals-and-strategies/), [3](https://medium.com/@s_m_i/lessons-in-inclusive-hiring-what-ive-learnt-d8501d8925d5).

### Take-home interviews are unethical

Take-home tests are unfair to the candidate unless we pay them for the work. [The issues surrounding take-home tests are covered in this op-ed.](https://www.nytimes.com/2010/12/04/your-money/04shortcuts.html)

### Non-verbal communication

We should try to meet with the candidate in person as much as possible. If that's not possible, we should video chat with them. [Non-verbal communication is a large part of collaboration.](https://www.thebalance.com/nonverbal-communication-in-the-workplace-1918470) If we only use phone calls, we eliminate entire channels of communication like gestures and eye contact, which makes it more difficult for both the candidate and the interviewer.

### Interview lengths

The interviews earlier in the pipeline should be shorter than ones that come later. This way, we can more quickly filter out candidates who are not a good fit for the role without too much time invested in the process. Ideally, we would do a quick phone chat early in the process to gauge how well the candidate would do in the rest of the interviews.

## Closing thoughts

The overarching philosophy of designing this pipeline, for me, was to start with the actual role and work backwards. I started by asking, "one year from now, what kind of person would we consider a successful hire for this role?" Then, I tried to design a pipeline that this person would pass with flying colors, while most others would at least show some red flags. By keeping the questions as close to the real problems as possible, we are removing possiblities that the questions are a poor selector of candidates.

It's challenging to talk about an interview pipeline I designed without giving away too many details about the acutal questions and topics we cover. However, I hope that by talking openly about the ideas that informed my decisions about the pipeline, it helps others in the startup community to design effective and empathetic interview pipelines for whatever role they need.