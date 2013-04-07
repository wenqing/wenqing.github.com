---
layout: page
tagline: Supporting tagline
---

<h2>Archives</h2>
<ul>
  {% for post in site.posts %}

    {% unless post.next %}
      <h3>{{ post.date | date: '%Y' }}</h3>
    {% else %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
      {% if year != nyear %}
        <h3>{{ post.date | date: '%Y' }}</h3>
      {% endif %}
    {% endunless %}

    <li><span>
     {{ post.date | date_to_string }}</span> &raquo;
       <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}
      <img src="{{ post.image }}" />
      </a> 
   </li>

  {% endfor %}
</ul>

