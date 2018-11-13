---
layout: shirts
title: Bas testing
permalink: /bas/
---

{% for bas in site.bas %}
  <h2>
    <a href="{{ bas.url }}">
      {{ bas.title }}
    </a>
  </h2>
<!--  <p>{{ bas.content }}</p> -->
{% endfor %}

<ul class="tag-box inline">
{% assign list = site.bas | sort %}
    {% for bandname in list %} 
        <li>
            <a href="#{{ bandname[0] }}">
                {{ bandname[0] }}
            </a>
            <span>({{ bandname[1].size }})</span>
        </li>
    {% endfor %}
{% assign list = nil %}
</ul>

{% assign taglist = site.bas | sort %}
{% for bandname in taglist %} 
 <h2 id="{{ bandname[0] }}">{{ bandname[0] }}</h2>
 <ul class="post-list">
  {% assign list = bandname[1] %}  
  {% for post in list %}
   <li>
   <a href="{{ post.url }}">{{ post.title }}</a>
   </li>
  {% endfor %}
  {% assign pages_list = nil %}
  {% assign group = nil %}
 </ul>
{% endfor %}
{% assign taglist = nil %}