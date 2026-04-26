<h2 id="publications" style="margin: 2px 0px 20px;">Publications</h2>

<div class="publications">
<ul class="bibliography" style="list-style: none; padding: 0; margin-bottom: 20px;">

{% for link in site.data.publications.papers %}

<li style="margin-bottom: 25px;">
  <div style="border-left: 3px solid #4a90e2; padding-left: 15px;">
      <div class="title" style="font-size: 1.1em; font-weight: 600; margin-bottom: 4px;">
        <a href="{{ link.page | default: link.pdf }}" target="_blank" style="text-decoration: none;">{{ link.title }}</a>
      </div>
      <div class="author" style="margin-bottom: 4px; font-size: 0.95em;">{{ link.authors }}</div>
      <div class="periodical" style="margin-bottom: 8px;"><em>{{ link.conference }}</em></div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.paper_pdf %} 
      <a href="{{ link.paper_pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Paper</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</li>

{% endfor %}

</ul>
</div>

<h2 id="posters" style="margin: 5px 0px 20px;">Poster Presentations</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.posters %}

<li>
<div class="pub-row" style="margin-bottom: 20px;">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% endif %}
    {% if link.conference_short %} 
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title">
        {% if link.page %}
        <a href="{{ link.page }}" target="_blank">{{ link.title }}</a>
        {% elsif link.pdf %}
        <a href="{{ link.pdf }}" target="_blank">{{ link.title }}</a>
        {% else %}
        {{ link.title }}
        {% endif %}
      </div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.paper_pdf %} 
      <a href="{{ link.paper_pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Paper</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>

{% endfor %}

</ol>
</div>