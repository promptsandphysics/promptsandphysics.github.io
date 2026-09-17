---
layout: page
title: Newsfeed
permalink: /newsfeed/
subtitle: Things worth knowing about, and places where this argument is happening elsewhere.
---

A running log of developments at the intersection of theoretical physics and
machine learning, plus links to where the discussion is taking place outside
this site. Not remotely exhaustive — if something belongs here, tell us at
[{{ site.email }}](mailto:{{ site.email }}).

## Recent

{% assign items = site.data.newsfeed | sort: "date" | reverse %}
{% for item in items %}
<article class="news-item">
  <p class="post-meta">
    <time datetime="{{ item.date }}">{{ item.date | date: "%-d %B %Y" }}</time>
    {% if item.sample %}<span class="flag-sample">example</span>{% endif %}
  </p>
  <h3 class="news-title">
    {% if item.url %}<a href="{{ item.url }}">{{ item.title }}</a>{% else %}{{ item.title }}{% endif %}
  </h3>
  <p>{{ item.summary }}</p>
</article>
{% endfor %}

## Elsewhere

{% for link in site.data.links %}
- [{{ link.title }}]({{ link.url }}) — {{ link.note }}
{% endfor %}
