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
	  </li>
	<!--  <p>{{ bas.content }}</p> -->
	{% endfor %}
</ul>
