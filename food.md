---
layout: food
title: "food Posts"
permalink: /food/
---

<ul class="posts">
    {% for post in site.categories.food %}
        <li>
            <span class="post-date">{{ post.date | date: "%b %d, %Y" }}</span>
            ::
            <a class="post-link" href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
            @ {
            {% assign tag = post.tags | sort %}
            {% for category in tag %}<span><a href="{{ site.baseurl }}category/#{{ category }}" class="reserved">{{ category }}</a>{% if forloop.last != true %},{% endif %}</span>{% endfor %}
            {% assign tag = nil %}
            }
        </li>
    {% endfor %}
</ul>
