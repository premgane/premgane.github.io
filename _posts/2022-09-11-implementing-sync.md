---
layout:     post
title:      "Reimplementing go's sync package"
date:       2022-09-11 11:57:00
summary:    "Using only golang's channels, you can implement the entire sync package."
tags:       go programming problem-solving
---

[This blog post from 2019, despite its unassuming name (*Go advanced concurrency patterns: part 3 (channels)*)](https://blogtitle.github.io/go-advanced-concurrency-patterns-part-3-channels/), is something I found delightful and enlightening.

## Background

Go has a package called `sync` in its standard library. It contains a few useful tools like `Mutex` and `WaitGroup`, allowing for traditional concurrency patterns in your code. These are called the concurrency primitives. They're definitely useful if you're thinking in the traditional object-oriented way -- for example, if you're coming from Java like I was.

However, a principle in idiomatic Go is to "Share by communicating." You'll see this repeated in many places. What this means is that when your instinct is to look for a primitive that will satisfy your requirements, see if there's a way to [use channels to send data to goroutines](https://golangdocs.com/channels-in-golang) instead.

The above blog post takes the primitives in the `sync` package and implements each one using channels. This is a simple and effective demonstration of how expressive channels truly are. It's hard to appreciate channels, which seem like not that big of a deal at first glance, until you see idiomatic code like this.

## Other resources

If you're not so familiar with how concurrency works in Go, here are some resources I've found useful.

[This post](https://teivah.medium.com/a-closer-look-at-go-sync-package-9f4e4a28c35a) is pretty good at introducing you to the `sync` package in case you need a reference other than [the excellent docs](https://pkg.go.dev/sync).

If you'd like a primer on concurrency patterns in Go, I recommend this book: [Concurrency in Go, by Katherine Cox-Buday](https://www.oreilly.com/library/view/concurrency-in-go/9781491941294/).

## Closing thoughts

[*Go advanced concurrency patterns: part 3 (channels)*](https://blogtitle.github.io/go-advanced-concurrency-patterns-part-3-channels/), given me a new perspective on concurrency, not just in Go, but as a concept generally. I will continue to make fun of its unwieldy title, though.

Even if you don't program in Go, I'd recommend that you take a look at the entire [series of posts](https://blogtitle.github.io/categories/concurrency/), each of which is interesting in its own way.