---
layout: post
title: "First Blog"
date: 2014-03-24 17:37:02 +0800
comments: true
categories: 
---
#Blog

##Installation

Blog framework:Octopress

```
http://octopress.org
```

###install octopress

* install git

* install rbenv

* clone octopress from github

```
git clone git://github.com/imathis/octopress.git octopress
```

* install dependencies

```
gem install bundler
rbenv rehash    # If you use rbenv, rehash to be able to run the bundle command
bundle install
```

* Install the default Octopress theme

```
rake install
```

###deploying to Github Pages

* Create a new Github repository and name the repository with the format username.github.io, where username is your GitHub user name or organization name.

* input

```
rake setup_github_pages
git@github.com:wwwcevon/wwwcevon.github.io.git
```

* Next run:

```
rake generate
rake deploy
```

* commit the source for your blog.

```
git add .
git commit -m 'your message'
git push origin source
```

###Configuring Octopress

```
 _config.yml       # Main config (Jekyll's settings)
Rakefile          # Configs for deployment
config.rb         # Compass config
config.ru         # Rack config
```

......http://octopress.org/docs/configuring/

###BLog with Octopress

* rake new_post["title"]

* Generate and preview

```
rake generate   # Generates posts and pages into the public directory
rake watch      # Watches source/ and sass/ for changes and regenerates
rake preview    # open in chrome
```
