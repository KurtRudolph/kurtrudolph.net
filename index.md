---
layout: page
---
<div class="alert"><big>Under Construction</big></div>

<div class="hero-unit">
<h1>My homepage!</h1>
</div>


<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> 
    &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>



