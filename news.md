---
layout: default
title: News
---

<h2>HexChat News - <a href="http://feeds.feedburner.com/hexchat" rel="alternate" type="application/atom+xml"><img class="rss-icon" src="/img/feed-icon20x20.png" width="20" height="20" alt="Feed"/></a></h2>

{% for post in site.posts %}
<h3><a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date_to_string }}</h3>
{% endfor %}