<h2 id="publications" class="section-title">Publications</h2>

<div class="publications-list">
{% for link in site.data.publications.main %}
  <div class="pub-card">
    {% if link.image %}
    <div class="pub-image">
      <img src="{{ link.image }}" alt="{{ link.title }}" class="teaser-img">
    </div>
    {% endif %}
    
    <div class="pub-content">
      <h3 class="pub-title">
        {% if link.pdf %}
          <a href="{{ link.pdf }}" target="_blank" rel="noopener noreferrer">{{ link.title }}</a>
        {% elsif link.page %}
          <a href="{{ link.page }}" target="_blank" rel="noopener noreferrer">{{ link.title }}</a>
        {% else %}
          {{ link.title }}
        {% endif %}
      </h3>

      <div class="pub-authors">{{ link.authors }}</div>
      
      <div class="pub-venue">
        <em>{{ link.conference }}</em>
      </div>

      <div class="pub-links">
        {% if link.pdf %}
          <a href="{{ link.pdf }}" class="btn-pub" target="_blank" rel="noopener noreferrer"><i class="far fa-file-pdf"></i> PDF</a>
        {% endif %}
        {% if link.code %}
          <a href="{{ link.code }}" class="btn-pub" target="_blank" rel="noopener noreferrer"><i class="fab fa-github"></i> Code</a>
        {% endif %}
        {% if link.page %}
          <a href="{{ link.page }}" class="btn-pub" target="_blank" rel="noopener noreferrer"><i class="fas fa-globe"></i> Project Page</a>
        {% endif %}
        {% if link.bibtex %}
          <a href="{{ link.bibtex }}" class="btn-pub" target="_blank" rel="noopener noreferrer"><i class="fas fa-quote-right"></i> BibTeX</a>
        {% endif %}
        {% if link.notes %}
          <span class="badge-status">{{ link.notes }}</span>
        {% endif %}
        {% if link.others %}
          <span class="pub-others">{{ link.others }}</span>
        {% endif %}
      </div>
    </div>
  </div>
{% endfor %}
</div>