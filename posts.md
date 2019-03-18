---
layout: default
title: News
order: 2
---

# {{ page.title }}

<div>
<a class="button" href="/feed.xml">RSS Feed</a>
</div>
---

<div>
{% for post in site.posts limit:5 %}
<a href="{{ post.url }}"><h2>{{ post.title }}</h2></a>
<small>{{ post.date | date_to_long_string }}</small>
<p>{{ post.excerpt }}</p>
{% endfor %}
</div>