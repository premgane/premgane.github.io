---
layout:     post
title:      Reinstalling Bundle to run Jekyll
date:       2018-02-18 19:50:00
summary:    "Fixing a strange issue with Ruby gems to fix a 'bad interpreter' error"
categories: macos ruby gem
---

I use Jekyll for this blog, and this means dealing with Ruby in order to build this site on my local machine (a 2012 Macbook Pro).

Sometimes, like today, this can be troublesome.

When I tried to run my `bundle exec jekyll serve` command, I ran into this error:

{% highlight ruby lineanchors %}
zsh: /usr/local/bin/bundle: bad interpreter: /System/Library/Frameworks/Ruby.framework/Versions/2.0/usr/bin: no such file or directory
{% endhighlight %}

After Googling this error, I found this (somewhat unrelated) [issue on GitHub.](https://github.com/CocoaPods/CocoaPods/issues/6778)

From the discussion, I gathered that it's probably caused by my updating the version of Ruby on my machine, and I just need to reinstall the `bundle` gem. So, I did this but got the following error:

{% highlight ruby lineanchors %}
% gem install bundle
Fetching: bundler-1.16.1.gem (100%)
ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /Library/Ruby/Gems/2.3.0 directory.
{% endhighlight %}

So, I needed to update the owner of that directory and all its subdirectories:

{% highlight ruby lineanchors %}
% sudo chown -R prem:wheel /Library/Ruby/Gems/2.3.0
% gem install bundle
{% endhighlight %}

Then, finally, I found out that I had to reinstall `bundle` altogether:

{% highlight ruby lineanchors %}
% rm Gemfile.lock
% bundle install
{% endhighlight %}