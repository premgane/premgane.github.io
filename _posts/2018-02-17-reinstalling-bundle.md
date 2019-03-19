---
layout:     post
title:      Reinstalling Bundle to run Jekyll
date:       2018-02-18 19:50:00
summary:    "Fixing a strange issue with Ruby gems to fix a 'bad interpreter' error"
tags:       macos ruby gem
---

I use Jekyll for this blog, and this means dealing with Ruby in order to build this site on my local machine (a 2012 Macbook Pro running MacOS 10.13.3, High Sierra).

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

Next, I had to add the following to my `Gemfile`:

{% highlight ruby lineanchors %}
gem 'ffi', '1.9.18'

gem 'nokogiri', '1.8.1'
gem 'pkg-config'
{% endhighlight %}

`ffi` is explained in [this GitHub issue.](https://github.com/ffi/ffi/issues/608#issuecomment-364335111) As for the other two libraries, I had to add them through trial and error. To be honest, I'm not entirely sure if they were necessary, but they were one of the multitude of approaches I tried to get Jekyll working again.

I also needed to manually install `nokogiri` by following the instructions on [their documentation page.](http://www.nokogiri.org/tutorials/installing_nokogiri.html) Specifically, I had to do the following:

{% highlight ruby lineanchors %}
gem update --system
xcode-select --install # Then agree to the terms, even if you have done this before!
bundle config build.nokogiri --use-system-libraries \
  --with-xml2-include=$(brew --prefix libxml2)/include/libxml2
bundle install --path vendor/bundle
bundle update nokogiri
{% endhighlight %}

Now that `bundle` is installed in the `vendor` directory, I had to add `vendor` to my `.gitignore` so I don't check in all the packages.

Along the way, I also had to run some `chown -R` commands to modify the owner of some directories here and there. If you are following along, it will be clear from the error messages when to do this.

I hope this helps someone else out there. All told, this took me over an hour to figure out.