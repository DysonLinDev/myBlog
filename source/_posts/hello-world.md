---
title: Hello Hexo!
date: 2020-04-13 20:50:40
tags: 
- Hexo
- Github
- Travis
---
# Hello [Hexo](https://hexo.io/)!

## Why Hexo 
Hexo is a decent and simple open source blog framework and it brings github page and travis CI togethe, which makes developers build your own blog in seconds. 

## Tips for Hexo beginners
Here's are some tips that official document probably doesn't metion:

### 1. Github page (gh-page)
Don't put your hexo code in master. Master branch is the one that github page uses to host your blog.

### 2. Travis yml
Following the document makes you confused if you haven't use travis before.

Here's some points that makes you more easier to setup.
```yaml
## .travis.yml
branches:
  only:
    - hexo # build hexo branch only
script:
  - hexo generate # generate static files
deploy:
  provider: pages
  skip-cleanup: true
  github-token: $GH_TOKEN
  keep-history: true
  target_branch: master # The one we put blog content 
  on:
    branch: hexo # The one we host hexo source
  local-dir: public
```

### 3. Theme and plugin
Now, your blog should be running and it's time to choose a good layout. 
[Theme](https://hexo.io/themes/) & [Plugin](https://hexo.io/plugins/) save you time.

### 4. Hot reload
One more thing, if you feel uncomfortable without auto-reload. 
Here is it: 

run
```
npm install hexo-browsersync --save
```
and do 'hexo server'. 

There you go!

```bash
$ hexo server
INFO  Start processing
[Browsersync] Access URLs:
 ----------------------------------
          UI: http://localhost:3001
 ----------------------------------
 UI External: http://localhost:3001
 ----------------------------------
INFO  Hexo is running at http://localhost:4000 . Press Ctrl+C to stop.
```


## The journey just starts!
Sharing knowledge and life with you. See you soon.

