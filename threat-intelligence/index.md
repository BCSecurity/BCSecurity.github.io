---
layout: default
title: "Threat Intelligence"
---

# Threat Intelligence

Below is a list of all posts categorized as Threat Intelligence Reports

{% comment %}
  We use Liquid to filter site.posts for any that include 'Threat-Intelligence'
  in their categories.
{% endcomment %}
{% assign threat_posts = site.posts | where_exp: "post", "post.categories contains 'Threat-Intelligence'" %}

{% if threat_posts.size > 0 %}
<ul>
  {% for post in threat_posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a> 
      <small>({{ post.date | date: "%B %d, %Y" }})</small>
    </li>
  {% endfor %}
</ul>
{% else %}
<p><em>No Threat Intelligence blogposts yet.</em></p>
{% endif %}
