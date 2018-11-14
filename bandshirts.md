---
layout: page
title: Band Shirts
permalink: /bandshirts/
---

<!--
	{% for category in bas.tags %}<span><a href="{{ site.baseurl }}categories/#{{ category }}" class="reserved">{{ category }}</a>{% if forloop.last != true %}&nbsp;{% endif %}</span>{% endfor %}
-->

<a href="{{ site.baseurl }}/shirts-image-heavy" class="reserved">Image heavy</a> for scrolling shirts.

<ul class="posts">

	{% for bandshirts in site.bandshirts %}
	  <li>
	    <a href="{{ bandshirts.url }}">
	      {{ bandshirts.title }}
	    </a>
	  </li>
	{% endfor %}
</ul>
