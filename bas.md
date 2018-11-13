{% for bas in site.bas %}
  <h2>
    <a href="{{ bas.url }}">
      {{ bas.title }}
    </a>
  </h2>
  <p>{{ bas.content }}</p>
{% endfor %}