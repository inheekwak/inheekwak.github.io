<h2 id="projects" class="pub-section-title">Projects</h2>

<h3 class="pub-subsection" style="margin: 30px 0px -30px;">All Projects</h3>

<div class="projects">
<ol class="bibliography">

{% for post in site.posts %}
  {% if post.categories contains "projects" %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if post.image %}<img src="{{ post.image }}" class="teaser img-fluid z-depth-1">{% endif %}
    {% if post.conference_short %}<abbr class="badge" data-venue="{{ post.conference_short }}">{{ post.conference_short }}</abbr>{% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
    <div class="title"><a href="{{ post.url }}">{{ post.title }}</a></div>
    {% if post.authors %}<div class="author">{{ post.authors }}</div>{% endif %}
    {% if post.conference %}<div class="periodical"><em>{{ post.conference }}</em></div>{% endif %}
    <div class="links">
      {% if post.pdf %} 
      <a href="{{ post.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if post.code %} 
      <a href="{{ post.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if post.page %} 
      <a href="{{ post.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if post.bibtex %} 
      <a href="{{ post.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if post.notes %} 
      <strong> <i style="color:#e74d3c; font-weight:600">{{ post.notes }}</i></strong>
      {% endif %}
    </div>
  </div>
</div>
</li>

  {% endif %}
{% endfor %}

</ol>
</div>
