---
layout: default
title: Blog
---

<div class="blog-posts">
 {% for post in site.posts %}
 {% assign author = site.authors[post.author] %}
 <div class="post" markdown="1">

## [{{ post.title }}]({{ post.url }})

<div class="post-info">
  Published on <span class="date">{{ post.date | date: "%B %e, %Y" }}</span> by
  <a class="author" href="http://twitter.com/{{author.twitter}}">
    {{ author.name }}
  </a>
</div>

<div class="post-content">
  {{ post.content }}
</div>

 </div>
 {% endfor %}
</div>

<div class="post-subscribe" markdown="1">
  Subscribe to this blog via
  [RSS]({{ site.rss_feed }}).
</div>
