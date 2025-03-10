---
layout: default
title: "IoCs"
---

# Indicators of Compromise (IoCs)

These posts are flagged with the "IoCs" category:

{% assign ioc_posts = site.posts | where_exp: "post", "post.categories contains 'IoCs'" %}

{% if ioc_posts.size > 0 %}
<ul>
  {% for post in ioc_posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a> 
      <small>({{ post.date | date: "%B %d, %Y" }})</small>
    </li>
  {% endfor %}
</ul>
{% else %}
<p><em>No IoCs-related posts yet.</em></p>
{% endif %}
