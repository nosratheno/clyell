---
layout: food
title: "Dinner Time"
permalink: /food/
---

<ul class="posts">
    {% for post in site.categories.food %}
        <li>
            <a class="post-link" href="{{ post.url }}">{{ post.title }}</a>
            [
            {% assign tag = post.tags | sort %}
            {% for category in tag %}<span><a href="{{ site.baseurl }}categories/#{{ category }}" class="reserved">{{ category }}</a>{% if forloop.last != true %}&nbsp;{% endif %}</span>{% endfor %}
            {% assign tag = nil %}
            ]
        </li>
    {% endfor %}
</ul>
