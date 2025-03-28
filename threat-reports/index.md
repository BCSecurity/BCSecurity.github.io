---
layout: default
title: "Threat Reports"
permalink: /threat-reports/
---

<h1>Threat Reports</h1>
<p>Check out the latest reports:</p>

{% assign threat_posts = site.posts | where_exp: "post", "post.categories contains 'Threat-Reports'" %}

{% if threat_posts.size > 0 %}
<div class="row row-cols-1 row-cols-md-3 g-4">
  {% for post in threat_posts %}
  <div class="col">
    <!-- Card with a dark background, white text, and subtle hover effect -->
    <div class="card h-100 border-0 hover-card" style="background-color: #2c2c2c; color: #ffffff;">
      <a href="{{ post.url | relative_url }}" class="card-link" style="text-decoration: none; color: inherit;">
        <!-- Display post image or a fallback image -->
        <img
          src="{{ post.image | default: '/assets/images/default.png' }}"
          class="card-img-top"
          alt="{{ post.title }}"
          style="object-fit: cover; height: 200px;"
        />
        <div class="card-body">
          <h5 class="card-title">{{ post.title }}</h5>
        </div>
      </a>
    </div>
  </div>
  {% endfor %}
</div>
{% else %}
<p><em>No Threat Reports yet.</em></p>
{% endif %}
