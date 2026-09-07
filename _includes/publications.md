<h2 id="publications">Publications</h2>

<ol>
{% for publication in site.data.publications.main %}
  <li class="publication-item">
    <div class="publication-card">
      {% if publication.image %}
      <a class="publication-figure" href="{{ publication.image_pdf | default: publication.image | relative_url }}" aria-label="View figure for {{ publication.title }}">
        <img src="{{ publication.image | relative_url }}" alt="Method overview for {{ publication.title }}">
        {% if publication.badge %}<span class="publication-badge">{{ publication.badge }}</span>{% endif %}
      </a>
      {% endif %}
      <div class="publication-details">
        {% if publication.pdf %}
        <strong><a href="{{ publication.pdf }}">{{ publication.title }}</a></strong><br>
        {% else %}
        <strong>{{ publication.title }}</strong><br>
        {% endif %}
        {{ publication.authors }}<br>
        <em>{{ publication.conference }}</em>
      </div>
    </div>
  </li>
{% endfor %}
</ol>
