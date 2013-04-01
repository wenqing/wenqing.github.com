---
layout: default
title: Achieve
tagline: Supporting tagline
---
<section class="Achieve">
  <h2>Achieve</h2>
</section>

<p>
<ul class="posts">
  {% for post in site.posts %}
    <li><span>
     {{ post.date | date_to_string }}</span> &raquo;
       <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}
      <img src="{{ post.image }}" />
      </a> 
   </li>
  {% endfor %}
</ul>
 
</p>
