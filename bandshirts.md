---
layout: page
title: Band Shirts
permalink: /bandshirts/
---

<!--
	{% for category in bas.tags %}<span><a href="{{ site.baseurl }}categories/#{{ category }}" class="reserved">{{ category }}</a>{% if forloop.last != true %}&nbsp;{% endif %}</span>{% endfor %}
-->

<ul class="posts">

	{% for bandshirts in site.bandshirts %}
	  <li>
	    <a href="{{ bandshirts.url }}">
	      {{ bandshirts.title }}
	    </a>
	  </li>
	{% endfor %}
</ul>
