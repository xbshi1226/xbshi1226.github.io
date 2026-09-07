<h2 id="publications">Publications</h2>

<div class="publication-list">
{% for publication in site.data.publications.main %}
  <article class="publication-item">
    <div class="publication-card">
      {% if publication.image %}
      <a class="publication-figure" href="{{ publication.image_pdf | default: publication.image | relative_url }}" aria-label="View figure for {{ publication.title }}">
        <img src="{{ publication.image | relative_url }}" alt="Method overview for {{ publication.title }}">
        {% if publication.badge %}<span class="publication-badge">{{ publication.badge }}</span>{% endif %}
      </a>
      {% endif %}
      <div class="publication-details">
        <div class="publication-title">{{ publication.title }}</div>
        <div class="publication-authors">{{ publication.authors }}</div>
        <div class="publication-links">
          <a href="{{ publication.pdf }}">PDF</a>
          <a href="{{ publication.code }}">Code</a>
        </div>
      </div>
    </div>
  </article>
{% endfor %}
</div>
