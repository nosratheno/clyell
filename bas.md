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

<ul class="posts">
    {% for bas in site.bas %}
        <li>
            ::
            <a class="post-link" href="{{ bas.url }}">{{ bas.title }}</a>
            [
            {% assign tag = bas.bandname | sort %}
            {% for category in tag %}<span><a href="{{ site.baseurl }}categories/#{{ category }}" class="reserved">{{ category }}</a>{% if forloop.last != true %}&nbsp;{% endif %}</span>{% endfor %}
            {% assign tag = nil %}
            ]
        </li>
    {% endfor %}
</ul>
