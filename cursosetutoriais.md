---
layout: page
title: Courses & Tutorials
subtitle: Some of the materials I used for teaching (in Portuguese)
---

<div>
{% assign postsCategory = site.posts | group_by_exp:"post", "post.categories"  %}
{% for category in postsCategory %}
<h4 class="post-teaser__month">
<strong>
{% if category.name %} 
[{{ category.name }}]
{% else %} 
{{ Print }} 
{% endif %}
</strong>
</h4>
<ul class="list-posts">
{% for post in category.items %}
<li class="post-teaser">
<a href="{{ post.url | prepend: site.baseurl }}">
<span class="post-teaser__title">{{ post.title }}</span>
</a>
</li>
{% endfor %}
</ul>
{% endfor %}
</div>