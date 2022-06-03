# MLC Robotics
This site is created based on a template provided by the [Bedford Lab](https://bedford.io/), the source code can be found [here](https://github.com/blab/blotter). Thank you [Trevor Bedford](https://bedford.io/team/trevor-bedford/) and the Bedford Lab. 

## Build site

To build the website locally, clone the repo with:

```
git clone https://github.com/blab/blotter.git
```

Then install necessary Ruby dependencies by running `bundle install` from within the `blotter` directory.  After this, the site can be be built with:

```
bundle exec jekyll build
```

(If you are getting errors at this stage, it may be due to your version of `bundle`. Try `gem uninstall bundler` + `gem install bundler -v 1.13.1`.)

To view the site, run `bundle exec jekyll serve` and point a browser to `http://localhost:4000/`.  More information on Jekyll can be found [here](http://jekyllrb.com/).

To include projects, preprocessing scripts are necessary to clone project repos and update Jekyll metadata. This can be accomplished with:

```
ruby _scripts/update-and-preprocess.rb
```

Then `jekyll build` works as normal.

## Contribute

Blog posts just require YAML top matter that looks something like:

```
---
layout: post
title: Newton Institute presentation
author: Trevor Bedford
link: http://www.newton.ac.uk/programmes/IDD/seminars/2013082213301.html
image: /images/blog/transmission.png
---
```

The `layout`, `title` and `author` tags are required, while `link` and `image` are optional.  Just save a Markdown file with this top matter as something like `blog/_posts/2013-08-27-newton-institute.md`, where `2013-08-27` is the date of the post and `newton-institute` is the short title.  This short title is used in the URL of the post, so this becomes `blog/newton-institute/`, so the short title should be long enough and unique enough not to cause conflicts with other posts.

## For more information

* Look over the [metadata format guide](http://mlc-robotics.github.io/guide/format/)
* Look over the [Markdown style guide](http://mlc-robotics.github.io/guide/style/)
