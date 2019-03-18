# ielab-web-template

welcome to the README file of the ielab-web-template. This file will get you set up and running to develop an ielab-themed website locally and explain how to add and edit content to the website.

## Edit locally
 
 Rather than guessing to see if your changes look good on the website without testing them, you can render the website locally with jekyll. **please follow [this tutorial](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/) to set this up**. Building the site locally gives you "hot-reloading" so you just need to refresh your browser to see changes.
 
## Site Configuration

Many common things about the site (such as the site title and description) can be configured in the `_config.yml` file. Adding links to github and twitter will place various links around the site. 
 
## Organisation of Website 

The organisation of the ielab website is currently broken down into the following collections:

 - people
 - posts
 - pages

### People

Example: [http://ielab.io/people/harry-scells](http://ielab.io/people/harry-scells)

People pages are located in the `_people` folder. The name of each file should correspond the the name of the person: e.g., `harry-scells.md`.

A person has the following variables (with example values):

```yaml
name: Person Display Name
image: /images/example.png
description: This is an example description.
role: role
twitter: //twitter.com/username
twitter-timeline: true
orcid: 0000-0000-0000-0000
github: //github.com/username
website: //example.com
scholar: //scholar.google.com.au/citations?user=EXAMPLE
``` 

The `name`, `image`, and `description` are used in most places in the website (e.g., home page and publications). The `role` determines where the person should fit in the home page. The values of `role` can either be `staff`, `phd`, or `external`. The `twitter-timeline` variable will place a timeline of tweets using the `twitter` variable on the profile page.

Content inside each person page can be anything that you wish to mention about yourself. Add content to your people page underneath the front matter. This content will appear after your name, links, and description, but before your publications.

### Posts

Example: [http://localhost:4000/posts/2019/01/30/journal-accepted-jmir.html](http://localhost:4000/posts/2019/01/30/journal-accepted-jmir.html)

Post pages are located in the `_posts` folder. The name of each file **must** adhere to the [jekyll specification](https://jekyllrb.com/docs/posts/) (i.e., `YEAR-MONTH-DAY-title.MARKUP`).

A post has the following variables:

```yaml
layout: post
title: "We have a README! You should read it!"
date: 2019-02-06
categories: posts
author: ielab team
tags: [publications]
```

The `layout` variable must be `post`. The `title`, `date` and `author` are displayed when templating the page. Enter content of the post underneath the front matter. The first paragraph of a post is used as an except in templating.

### Pages

If you have a requirement for a page at the top-level of the ielab website, just create a new page similar to `example.md`. The side bar will automatically include this as a top-level page.