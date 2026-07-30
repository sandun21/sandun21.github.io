<h2 id="publications" style="margin: 10px 0px 15px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-row">
  <div class="pub-content">
    <div class="title">
      {% if link.pdf %}
        <a href="{{ link.pdf }}" target="_blank">{{ link.title }}</a>
      {% elsif link.page %}
        <a href="{{ link.page }}" target="_blank">{{ link.title }}</a>
      {% else %}
        {{ link.title }}
      {% endif %}
    </div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
    <div class="links">
      {% if link.pdf %}<a href="{{ link.pdf }}" target="_blank">[PDF]</a>{% endif %}
      {% if link.code %}<a href="{{ link.code }}" target="_blank">[Code]</a>{% endif %}
      {% if link.page %}<a href="{{ link.page }}" target="_blank">[Project Page]</a>{% endif %}
      {% if link.bibtex %}<a href="{{ link.bibtex }}" target="_blank">[BibTeX]</a>{% endif %}
      {% if link.notes %}<em style="color:#e74d3c;">{{ link.notes }}</em>{% endif %}
      {% if link.others %}{{ link.others }}{% endif %}
    </div>
  </div>
</div>
</li>

{% endfor %}

</ol>
</div>