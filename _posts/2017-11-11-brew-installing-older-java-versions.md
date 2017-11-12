---
layout:     post
title:      Installing an older version of Java on OSX using Homebrew
date:       2017-11-11 16:50:00
summary:    "How to use Homebrew Caskroom to install Java 8"
categories: osx brew homebrew
---

Homebrew is an extremely useful tool until it isn't. Sometimes, it can hinder you.

For example, I was trying to install [Bazel](https://bazel.build/), which is required to run an [image-captioning inference engine](https://github.com/premgane/models/blob/master/research/im2txt/README.md#generating-captions) I was trying to run. Brew had some issues I needed to work through. Here is the story:

{% highlight sh lineanchors %}
brew install bazel                    
bazel: Java 1.8+ is required to install this formula.
JavaRequirement unsatisfied!

You can install with Homebrew-Cask:
  brew cask install java

You can download from:
  https://www.oracle.com/technetwork/java/javase/downloads/index.html
Error: An unsatisfied requirement failed this build.
{% endhighlight %}


Bazel, as of right now, no longer supports Java 7 and below. It only supports Java 8. Great, that's fine, I'll just use `brew cask install java` like it told me to.


{% highlight sh lineanchors %}
% brew cask install java                
==> Caveats
This Cask makes minor modifications to the JRE to prevent issues with
packaged applications, as discussed here:

  https://bugs.eclipse.org/bugs/show_bug.cgi?id=411361

If your Java application still asks for JRE installation, you might need
to reboot or logout/login.

Installing this Cask means you have AGREED to the Oracle Binary Code
License Agreement for Java SE at

  https://www.oracle.com/technetwork/java/javase/terms/license/index.html

==> Satisfying dependencies
==> Downloading http://download.oracle.com/otn-pub/java/jdk/9.0.1+11/jdk-9.0.1_osx-x64_bin.dmg
######################################################################## 100.0%
==> Verifying checksum for Cask java
==> Installing Cask java
==> Running installer for java; your password may be necessary.
==> Package installers may write to any location; options such as --appdir are ignored.
Password:

==> installer: Package name is JDK 9.0.1
==> installer: Upgrading at base path /
==> installer: The upgrade was successful.
🍺  java was successfully installed!
{% endhighlight %}

Let's verify that we have the right versions of Java:

{% highlight sh lineanchors %}
% /usr/libexec/java_home -V             
Matching Java Virtual Machines (3):
    9.0.1, x86_64:	"Java SE 9.0.1"	/Library/Java/JavaVirtualMachines/jdk-9.0.1.jdk/Contents/Home
    1.7.0_67, x86_64:	"Java SE 7"	/Library/Java/JavaVirtualMachines/jdk1.7.0_67.jdk/Contents/Home
{% endhighlight %}

Then, I updated my `~/.zshrc` to have this line:

{% highlight sh lineanchors %}
export JAVA_HOME=$(/usr/libexec/java_home -v 9)
{% endhighlight %}

Then, I ran `source ~/.zshrc` to ensure this change gets picked up and `$JAVA_HOME` gets set to my Java 9 installation.

Great! I just installed Java 9. Bazel should be happy now. Let's try again:

{% highlight sh lineanchors %}
% brew install bazel                    
==> Downloading https://homebrew.bintray.com/bottles/bazel-0.7.0.sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring bazel-0.7.0.sierra.bottle.tar.gz
==> Caveats
Bash completion has been installed to:
  /usr/local/etc/bash_completion.d

zsh completions have been installed to:
  /usr/local/share/zsh/site-functions
==> Summary
🍺  /usr/local/Cellar/bazel/0.7.0: 10 files, 95.0MB
{% endhighlight %}

Perfect! Now, let me try to use Bazel:

{% highlight sh lineanchors %}
bazel build -c opt //im2txt:run_inference
Problem with java installation: couldn't find/access rt.jar in /Library/Java/JavaVirtualMachines/jdk-9.0.1.jdk/Contents/Home
{% endhighlight %}

[It looks like Bazel only supports Java 8.](https://github.com/bazelbuild/bazel/issues/3410) How unfortunate. Looks like we'll have to use Homebrew to install Java 8.

This led me down a rabbithole of trying to install older versions of Java using Homebrew. Eventually, I found the right Caskroom command I needed to run:

{% highlight sh lineanchors %}
brew tap caskroom/versions
brew cask search java
brew cask install java8
{% endhighlight %}

Let's verify again:

{% highlight sh lineanchors %}
% /usr/libexec/java_home -V             
Matching Java Virtual Machines (3):
    9.0.1, x86_64:	"Java SE 9.0.1"	/Library/Java/JavaVirtualMachines/jdk-9.0.1.jdk/Contents/Home
    1.8.0_152, x86_64:	"Java SE 8"	/Library/Java/JavaVirtualMachines/jdk1.8.0_152.jdk/Contents/Home
    1.7.0_67, x86_64:	"Java SE 7"	/Library/Java/JavaVirtualMachines/jdk1.7.0_67.jdk/Contents/Home
{% endhighlight %}

Once again, I needed to update my `~/.zshrc` to ensure `$JAVA_HOME` is correct:

{% highlight sh lineanchors %}
export JAVA_HOME=$(/usr/libexec/java_home -v 1.8)
{% endhighlight %}

Then, of course, I had to run `source ~/.zshrc` again.

Finally, after all this time spent trying to get my toolchain working, I was able to run the `bazel` command I needed:

{% highlight sh lineanchors %}
% bazel build -c opt //im2txt:run_inference
....................
INFO: Found 1 target...
Target //im2txt:run_inference up-to-date:
  bazel-bin/im2txt/run_inference
INFO: Elapsed time: 14.490s, Critical Path: 0.06s
{% endhighlight %}

I hope this helps someone else out there!