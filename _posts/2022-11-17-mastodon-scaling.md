---
layout:     post
title:      "Scaling Mastodon"
date:       2022-11-17 19:58:00
summary:    "The scaling issues that Mastodon instances are facing reveal a lot about how it's architected."
tags:       web software problem-solving
---

Recently, Mastodon instances had to deal with an unprecedented number of new user signups. I found two instructive blog posts about how admins have been dealing with this influx.

[Nora Codes, about how weirder.earth had to scale.](https://nora.codes/post/scaling-mastodon-in-the-face-of-an-exodus/)

[teknique, about how Free Radical solved scaling issues partially by throwing a Raspberry Pi into the mix.](https://blog.freeradical.zone/post/surviving-thriving-through-2022-11-05-meltdown/)

Both of them reveal the bottlenecks of Mastodon's architecture. Some parts of the architecture can handle much larger rates of activity than others. Allocating resources intelligently allows the instance to scale much further with the same hardware.

Both deal with the same problems in different ways, approaching it with different philosophies. It's taught me a lot not just about sysadmin skills but also software architecture in a more general sense.