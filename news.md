---
layout: default
title: News
---

<span><h2><a href="http://feeds.feedburner.com/hexchat" rel="alternate" type="application/atom+xml"><img src="http://www.feedburner.com/fb/images/pub/feed-icon32x32.png" alt="rss-icon" style="vertical-align:middle;border:0" /></a> HexChat News</h2></span>

{% for post in site.posts %}
<h3><a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date_to_string }}</h3>
{% endfor %}