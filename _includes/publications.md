<h2 id="publications">Publications</h2>

<ol>
{% for publication in site.data.publications.main %}
  <li>
    {% if publication.pdf %}
    <strong><a href="{{ publication.pdf }}">{{ publication.title }}</a></strong><br>
    {% else %}
    <strong>{{ publication.title }}</strong><br>
    {% endif %}
    {{ publication.authors }}<br>
    <em>{{ publication.conference }}</em>
  </li>
{% endfor %}
</ol>
