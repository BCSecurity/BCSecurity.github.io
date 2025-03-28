---
layout: default
title: "Threat Reports"
permalink: /threat-reports/
---

<h1>Threat Reports</h1>
<p>Below is a list of all posts categorized as Threat Reports:</p>

{% assign threat_posts = site.posts | where_exp: "post", "post.categories contains 'Threat-Reports'" %}

{% if threat_posts.size > 0 %}
<div class="row row-cols-1 row-cols-md-3 g-4">
  {% for post in threat_posts %}
    <div class="col">
      <div class="card h-100">
        <!-- Display the post’s image if available, or use a default -->
        <img 
          src="{{ post.image | default: '/assets/images/default.png' }}" 
          class="card-img-top" 
          alt="{{ post.title }}" 
          style="object-fit: cover; height: 200px;" 
        />
        <div class="card-body">
          <h5 class="card-title">{{ post.title }}</h5>
          <!-- You can show an excerpt or a short description here if you like -->
          <p class="card-text">{{ post.excerpt }}</p>
          <a href="{{ post.url | relative_url }}" class="btn btn-primary">Read More</a>
        </div>
      </div>
    </div>
  {% endfor %}
</div>
{% else %}
<p><em>No Threat Reports yet.</em></p>
{% endif %}
