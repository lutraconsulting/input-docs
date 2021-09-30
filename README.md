# InputApp Help Center

This repository contains source files for the InputApp Help Center - https://help.inputapp.io/

The site is built with Jekyll and auto-deployed using GitHub Pages from `gh-pages` branch.

<div><img align="left" width="45" height="45" src="https://raw.githubusercontent.com/MerginMaps/docs/main/src/.vuepress/public/slack.svg"><a href="https://merginmaps.com/community/join">Join our community chat</a><br/>and ask questions!</div>

# For Developers

## Locally
1. Make sure you have Ruby installed
2. Install the jekyll and bundler gems:
   ```
   gem install jekyll bundler
   ```
3. Install this project's dependencies based on the `Gemfile`:
   ```
   bundle install
   ```
4. Start serving the web on your localhost:
   ```
   bundle exec jekyll serve
   ```
5. Go to http://localhost:4000/ in your browser

## With docker

```
  docker run --name linput-docs-dev \
  --rm --volume=`pwd`/www:/srv/jekyll \
  -e JEKYLL_ENV=development -p 35729:35729 \
  -p 4000:4000 -it jekyll/builder:4.1.0 jekyll serve
```

and go to http://localhost:4000/ in your browser

