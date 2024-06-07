# ITSC 2024 Reproducibility in Transportation Research: A Hands-on Tutorial

## Modify the page

For **Overview** and **Call for papers** and other sections, edit `index.md`.

To add a **Speaker**, add a `_speakers/someone.md` page.

There will be **Schedule** and **Papers** pages after the workshop proposal is accepted.

## Deploy the page

The page should update live in about a minute on https://rrintransportation.github.io/itsc24-rr-tutorial/ when you push to main branch.

The GitHub Action is set up following instructions in https://jekyllrb.com/docs/continuous-integration/github-actions/. You don't have to worry about it.

## (Optional) Serve the page locally

If you want to preview your edits locally, e.g. for changing css or adding new pages, follow this section to install the dependencies.

Install [Ruby](https://www.ruby-lang.org/en/downloads/), [Bundler](https://bundler.io/), and Jekyll. For ease of managing ruby gems, consider using [rbenv](https://github.com/rbenv/rbenv)*). Why Jekyll? Read this [blog post](https://karpathy.github.io/2014/07/01/switching-to-jekyll/)!

```
## on macOS, somehow I have to use sudo for `gem`
brew install ruby
brew install rbenv ruby-build
sudo gem install bundler jekyll
```

Serve the website

```bash
$ git clone git@github.com:RRinTransportation/itsc24-rr-tutorial.git
$ cd itsc24-rr-tutorial
$ sudo bundle install
$ bundle exec jekyll serve
## if I want instant update while I make changes to md files
$ sudo bundle exec jekyll serve --incremental --trace
```

## Template credits

This website template is based on original template provided by [Krishna Murthy Jatavallabhula](https://github.com/krrish94) and the modified version by [Zhutian Yang](https://github.com/zt-yang).