---
layout: page
title: "Album of the Month"
permalink: /albums/
---

<ul class="posts">
    {% for post in site.categories.aotm %}
        <li>
            <a class="post-link" href="{{ post.url }}">{{ post.title }}</a>
        </li>
    {% endfor %}
</ul>

<!--
* [November 2018]({{ site.baseurl }}albums/november-2018)
* [October 2018]({{ site.baseurl }}albums/october-2018)
-->
