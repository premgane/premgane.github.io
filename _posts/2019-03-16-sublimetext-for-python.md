---
layout:     post
title:      How to set up Sublime Text 3 for Python development
date:       2019-03-16 20:15:00
summary:    "Sublime Text 3 is a powerful IDE with some Python plugins."
categories: programming python
---

Recently, I reconsidered my Sublime Text setup for programming in Python. I wanted to know the latest best practices, shortcuts, and plugins. Here are the results of my research.

## Plugins

The most important plugin you should install right away is [Anaconda](https://damnwidget.github.io/anaconda/#). Spend some time reading the docs. This plugin converts Sublime Text 3 (ST3) into an effective Python IDE.

These articles list many useful plugins you should consider.

-  [Setting up Sublime Text 3 for full-stack Python development](https://realpython.com/setting-up-sublime-text-3-for-full-stack-python-development/#customizing-sublime-text-3). This is a good guide to get started setting up your ST3 workspace.
- [Super-charge your Sublime Text 3 to increase your productivity](https://hackernoon.com/super-charge-your-sublime-text-3-to-increase-your-productivity-5d02c2c1b356) This one is basically an exhaustive list of options.
- [Sublime Text 3 as Python IDE](https://mutux.com/2019/01/13/sublime-text-3-as-a-simple-python-ide.html). This page gives you an exhaustive list of preferences you should set up.

Note: if you install the Anaconda plugin, you don't need to install SublimeJEDI. They are both based on the same engine, and will cause plugin collision issues.

The way I approached this list is by installing almost all of these, then figuring out which ones I like the most. To keep things clean, I uninstalled all the plugins I found least useful.

## Shortcuts

First off, I would recommend this [useful tab management plugin called Origami](https://github.com/SublimeText/Origami). I'm learning these shortcuts and they have been invaluable so far.

[This cheat sheet](http://sweetme.at/2013/08/08/sublime-text-keyboard-shortcuts/) neatly lists all of the most useful Sublime Text shortcuts.

If you feel comfortable with Vim or `vi`, you may want to [enable Vintage mode](https://www.sublimetext.com/docs/3/vintage.html). Despite my familiarity with Vim, I found it annoying. But it's really a personal preference.

## My setup

- Anaconda
- GitGutter
- Origami
- Python3
- requirementstxt
- SideBarEnhancements
- SublimeLinter
- SublimeLinter-pep8
- SublimeLinter-pycodestyle
- SublimeLinter-pyflakes

You can install all of these using [Package Control](https://packagecontrol.io/).

In case you're interested, I use the [Spacegray Eighties](https://github.com/kkga/spacegray#spacegray-eighties) theme with the Gloom color scheme.
