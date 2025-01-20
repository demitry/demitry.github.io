---
layout: post
title:  "My Jekyll Setup"
date:   2025-01-18 21:17:00 +0200
categories: jekyll update
---

# My Jekyll Setup

## 1. Setup you Ruby Dev Env
To setup you Ruby development environment on Windows:
1. Install Ruby via RubyInstaller: [http://rubyinstaller.org/downloads/](http://rubyinstaller.org/downloads/)
2. Check your ruby version: Start - Run - type in `cmd` to open a windows console
3. Type in `ruby -v`
4. You will get something like that: `ruby 2.0.0p353 (2013-11-22) [i386-mingw32]`

## 2. Create and clone github repo

## 3. Setup Jekyll

```
gem install bundler jekyll
jekyll new my-awesome-site
cd my-awesome-site

# fix Gemfile, add lines
# TODO: Remove when this gets fixed in Jekyll
gem "csv"
gem "base64"

bundle install

bundle exec jekyll serve

#  => Now browse to http://localhost:4000
```

Test end


