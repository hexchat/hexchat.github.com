---
layout: default
title: News
---

<h2>HexChat News - <a href="http://feeds.feedburner.com/hexchat" rel="alternate" type="application/atom+xml"><img src="http://www.feedburner.com/fb/images/pub/feed-icon32x32.png" width="20" height="20" alt="rss-icon" style="vertical-align:-7%;border:0" /></a></h2>

{% for post in site.posts %}
<h3><a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date_to_string }}</h3>
{% endfor %}