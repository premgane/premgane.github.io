My personal site, http://premgkumar.com

# To install

Follow the instructions on [the official Jekyll installation docs page](https://jekyllrb.com/docs/installation/macos/)

```sh
bundle install
```

# To build

```sh
bundle exec jekyll build
```

Maybe use `--watch` if you want it to build every time you make a change to the build. But this is not necessary.

# To run

```sh
bundle exec jekyll serve
```

This will periodically check your markdown and regenerate the HTML.

# To update

```sh
gem update bundler
bundle update github-pages
```

This will grab all the latest package versions that [`github-pages`](https://github.com/github/pages-gem) requires.