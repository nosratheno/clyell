---
layout: shirts
title: Bas testing
permalink: /bas/
---

<ul class="posts">

	{% for bas in site.bas %}
	  <li>
	    <a href="{{ bas.url }}">
	      {{ bas.title }}
	    </a>
	     [
         {% assign tag = post.bandname | sort %}
         {% for category in tag %}<span><a href="{{ site.baseurl }}categories/#{{ category }}" class="reserved">{{ category }}</a>{% if forloop.last != true %}&nbsp;{% endif %}</span>{% endfor %}
         {% assign tag = nil %}
         ]
	  </li>
	{% endfor %}
</ul>
