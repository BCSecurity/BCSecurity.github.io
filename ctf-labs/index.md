---
layout: default
title: "CTF / Labs"
---

# CTF / Labs

Check out all posts labeled "CTF-Labs":

{% assign ctf_posts = site.posts | where_exp: "post", "post.categories contains 'CTF-Labs'" %}

{% if ctf_posts.size > 0 %}
<ul>
  {% for post in ctf_posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a> 
      <small>({{ post.date | date: "%B %d, %Y" }})</small>
    </li>
  {% endfor %}
</ul>
{% else %}
<p><em>No CTF or Lab posts yet.</em></p>
{% endif %}
First labs
