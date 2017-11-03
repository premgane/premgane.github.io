---
layout:     post
title:      Setting up a Python workspace
date:       2017-11-09 23:16:00
summary:    "An efficient use of PyEnv and Jupyter"
categories: programming python
---

[I found this post to be extremely useful.](https://medium.com/@henriquebastos/the-definitive-guide-to-setup-my-python-workspace-628d68552e14)

Basically, it contains instructions to set up PyEnv in a way that we have one Jupyter notebook that works with multiple Python interpreters.

One caveat: make sure your `~/.bashrc` or `~/.zshrc` does not contain any lines that mess with `$PYTHONPATH`. I haven't been able to get this setup working if I have something like the following in my `~/.zshrc`:

```
PYTHONPATH=/Users/prem/whatever/:$PYTHONPATH
```

I think it interferes with the way `pyenv` finds the location of `site-packages`.