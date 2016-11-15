---
layout:     post
title:      The 4 Common Failure Modes of Team Communication
date:       2016-11-14 08:42:00
summary:    These are the most commonly-occurring types of miscommunication in software engineering teams.
categories: teams communication
---

<blockquote>
  <p>
    Happy families are all alike; every unhappy family is unhappy in its own way.
  </p>
  <footer><cite title="Leo Tolstoy">Leo Tolstoy</cite></footer>
</blockquote>

Working with others can be a rewarding and illuminating experience. You learn much more than working by yourself. But communication can sometimes go wrong.

Teams that have trouble talking to each other might function at an acceptable level for a while. However, after some time, they will start to see a variety of issues:

- changes to system frequently breaks downstream systems
- production issues are left undiscovered or unfixed
- meetings are often a source of frustration and arguments

Effective communication feels effortless in a team where certain practices are habitual. These habits become second nature to the point where they become difficult to recognize.

Similarly, it is also hard to recognize that your team is communicating poorly. Everyone accepts that the team is supposed to communicate that way. Nobody can really imagine what it would be like to have a well-functioning team.

This post's purpose is to enumerate the 4 most common ways in which communication breaks down. The following is a compilation of my observations of teams I've worked with. I have also included some mitigation tactics that I've used successfully.

Let's dive in.

# 1. Arguing over observable facts

Sometimes, two team members come to a disagreement about something in the world. If this is easily observable or measurable, then the disagreement should be tabled until after the subject is measured.

## Example conflict

Alice asks Bob for some help writing a SQL query. Bob tells Alice that it's not possible to write such a query. Alice disagrees, and tells Bob that she's actually seen a similar query before. Bob gets frustrated and feels that Alice doesn't respect his experience. Alice gets frustrated that Bob doesn't believe her.

## Symptoms

- You are in an argument about a fact.
- Each person in the argument is 100% certain they are correct.
- The person you're arguing with appears to not believe or trust you.
- The person you're arguing with is totally wrong.

## Mitigation tactics

- Recognize that you're arguing. Stop.
- Try not to get aggravated at the other person. Don't let being right be your first priority.
- Go and observe who's right. Do it with the intention of getting to the truth, not proving the other person wrong.
- If you're in the middle of an unrelated meeting, jot it down and look it up later. Don't derail a meeting to go look it up.
  - If it's a blocking issue, plan for both contingencies: how to proceed if you're right vs. how to proceed if the other person is right.
- If you're graceful throughout the entire process, you should be happy to learn something new.
- If the other person turns out to be mistaken, let them save face by telling the story of how you came to learn this fact in the first place.

## Example resolution

Rather than continuing to argue, Alice shows Bob an example of a similar SQL query that she's run before. Bob realizes it actually is possible to write such a query, but he remembers this particular table doesn't have a certain index. They both come to an agreement that they should create this index, then Bob helps Alice write a query. They go get ice cream afterwards.

# 2. Arguing without understanding the context

An argument can arise when each person has the wrong mental model of the other person. This comes from a lack of context. Both people should step back and first communicate their context or understanding of the problem.

## Example conflict

During a meeting, Alice goes up to a whiteboard to sketch out her idea of an architecture for an interface to MongoDB. Bob believes she's about to sketch the architecture of a caching system that runs on top of MongoDB. He interrupts her to list the reasons why MongoDB is an extremely bad choice for a caching system. Alice feels frustrated that Bob trusts her so little that he wouldn't even let her finish.

## Symptoms

- You feel an urge to interrupt someone to shoot down what they're talking about. They are so obviously wrong that it's a waste of time to finish listening to them.
- You feel like the other person's position is so absurd that you have trouble believing they're for it.
- You feel like the other person's opinion is an attack on your own opinion.

## Mitigation tactics

- Recognize that you might be missing some key information. Stop arguing.
- Practice [steelmanning.](https://wiki.lesswrong.com/wiki/Steel_man) Try to come up, in your own mind, the strongest possible version of the other person's opinion.
- Explain back to the other person your understanding of their position. Include in your explanation what you think they're saying you should do next. End your explanation with a question to give the other person an opportunity to correct your understanding.
- Ask clarifying questions about some basic facts about the other person's opinion. Try not to sound condescending.
- Address the other person's underlying concerns before you bring up your own.

## Example resolution

Bob says, "So, what I'm seeing in your architecture is you're saying we should cache these objects in MongoDB. Is that what you meant?"

Alice answers, "Oh no, I don't think we should cache anything! I'm just trying to figure out how we should interface with our MongoDB cluster."

They go get ice cream afterwards.

# 3. Arguing about a topic after making unchecked assumptions

This is related to the previous issue but it's tougher. This issue is specifically about misunderstanding something in the real world, not someone's opinion.

In the previous issue, the source of the truth is in the other person's mind. A misunderstanding of a person can be solved by talking to that person. This issue, however, is harder to detect and maybe harder to solve.

## Example conflict

Alice and Bob are in a meeting to improve a certain page of the website that's been having problems. Bob has heard about this page in the daily stand up meetings, and he's formed some opinions about how they should fix it. He sees some obvious solutions and is glad they're finally getting around to fixing this page.

Alice, on the other hand, is the engineer who originally implemented this page. She knows in great detail why it's been having problems. She called this meeting to bounce some ideas off Bob.

Before Alice gets to present possible solutions, Bob gives his list of ideas. Before she can stop him, he begins to make plans on how to implement his ideas and their possible ramifications. Alice feels frustrated that her ideas aren't being considered at all. She also knows that Bob's ideas are uninformed and not at all feasible.

## Symptoms

- Something seems obvious to you but not to anyone else.
- Someone who should be more experienced than you in this context seems to have a hard time with something.
- Something that someone else says doesn't fit in with what you know.

## Mitigation tactics

- Recognize that you may be lacking context. Stop conjecturing.
- Ask clarifying questions. Give space to the other person to explain.
- Explain your understanding of the topic. Let the other person correct you.

## Example resolution

Bob says, "Thanks for asking for my input. I came into this meeting with some ideas based on what I've heard at standup this week. Should we get into them?"

Alice replies, "Sure, we'll get to them. But first, let's talk about exactly why this page has been having problems. I've talked about it a little bit at our standups, but I'd like to go into detail."

She proceeds to draw some diagrams on the whiteboard to explain how the page works. Bob learns some things that makes him realize that his original ideas weren't feasible. He knows they need to make some changes to make his ideas work, and those changes are too large to be practical. They work together to come up with a better idea.

They go get ice cream afterwards.

# 4. Having an argument where there isn't one

This category of arguments are difficult to stop once they're in motion because they're triggered by honest misunderstandings.

## Example conflict

Alice is happy to be working on UX enchancements on the Settings page. She's wanted to make improvements to this page for a long time. It's never been a priority for the team because not many users see it. She's finally made a strong enough case that her team has agreed this page needs work.

During standup the next day, she mentions she's working on UX improvements.

"I'm redesigning the Settings page," says Alice.

"Why?" asks Bob. He wasn't aware that the team had prioritized this page.

Alice thinks Bob is against this redesign. She feels attacked, especially because she fought hard to prioritize this redesign.

## Symptoms

- You are annoyed at a statement someone made because it implies something you don't like.
- You feel disrespected, and you notice that you feel defensive.
- You feel like you're being questioned for something you believe you're doing right.

## Mitigation tactics

- Recognize that you feel attacked. Decelerate the argument.
- Ask the other person to elaborate what they mean. Ask clarifying questions.
- If you're asked a question, start with the assumption that the other person simply wants to know the answer without ulterior motives.
- Ask yourself whether it's important that you win this argument here and now. What would happen if you lost? Probably not much.

## Example resolution

Alice says to Bob, "Well, the page is lagging behind the rest of the website. Why do you ask?"

Bob says, "Oh, I was just wondering. It's nice that we're finally getting the whole site up to speed."

They go get ice cream afterwards.

# Conclusion

Technical teams need to communicate well to function properly. When a team works well together, things get done on time, production issues are minimized, and everyone is less frustrated.

If your team does it right, none of you will notice it. However, teams that don't quite get it right will fail in their own unique ways. By learning to recognize the conditions under which your team fails, you can mitigate them. If you make these tactics habitual, you'll prevent these conditions from arising in the first place.