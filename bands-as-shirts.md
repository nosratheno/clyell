---
layout: shirts
title: "Bands as Shirts"
permalink: /bands-as-shirts/
---

<!--
<header>
    <h1>Category List</h1>
</header>

-->
<ul class="tag-box inline">
{% for page in site.categories.bandshirts %}
    {% assign list = site.tags.bandname | sort %}
    {% for category in list %}
        <li>
            <a href="#{{ category[0] }}">
                {{ category[0] }}
            </a>
            <span>({{ category[1].size }})</span>
        </li>
    {% endfor %}
{% endfor %}
{% assign list = nil %}
</ul>
