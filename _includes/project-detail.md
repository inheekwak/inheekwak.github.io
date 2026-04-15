<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ page.image }}" class="teaser img-fluid z-depth-1">
    {% if page.conference_short %}<abbr class="badge" data-venue="{{ page.conference_short }}">{{ page.conference_short }}</abbr>{% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
    <div class="title">{{ page.title }}</div>
    <div class="author">{{ page.authors }}</div>
    <div class="periodical"><em>{{ page.conference }}</em></div>
    <div class="links">
      {% if page.pdf %} 
      <a href="{{ page.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if page.code %} 
      <a href="{{ page.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if page.page %} 
      <a href="{{ page.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if page.data %} 
      <a href="{{ page.data }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Dataset</a>
      {% endif %}
      {% if page.bibtex %} 
      <a href="{{ page.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if page.notes %} 
      <strong> <i style="color:#e74d3c; font-weight:600">{{ page.notes }}</i></strong>
      {% endif %}
      {% if page.others %} 
      {{ page.others }}
      {% endif %}
    </div>
  </div>
</div>

{% if page.description %}
<div style="margin-top: 2rem; padding: 1rem; background-color: #f9f9f9; border-radius: 8px;">
  {{ page.description | markdownify }}
</div>
{% endif %}
