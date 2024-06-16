<h1 id="publications"></h1>

<h2 style="margin: 60px 0px -15px;">Publications <temp style="font-size:15px;">[</temp><a href="https://scholar.google.com/citations?user=S5XsBUMAAAAJ&hl=en&oi=ao" target="_blank" style="font-size:15px;">Google Scholar</a><temp style="font-size:15px;">]</temp><temp style="font-size:15px; margin-left: 10px;">[</temp><a href="https://orcid.org/0000-0002-0494-3538" target="_blank" style="font-size:15px;">Orcid</a><temp style="font-size:15px;">]</temp></temp><temp style="font-size:15px; margin-left: 10px;">[</temp><a href="https://www.webofscience.com/wos/author/record/37952318" target="_blank" style="font-size:15px;">Web of Science </a><temp style="font-size:15px;">]</temp>
</h2>

<h3 class="article" style="margin: 20px 0px -20px 20px; font-size: 20px">Articles</h3>
<!-- Articles Section -->
<div class="publications">
<ol class="bibliography">
{% assign counter = 1 %}
{% for link in site.data.publications.main %}
{% if link.type == "1" %}

<li>
<div class="pub-row">
<!--   <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
            <abbr class="badge">{{ link.conference_short }} {{ link.journal_short}}</abbr>
  </div> -->
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><span>{{ counter }}. </span><a href="{{ link.doi }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference}} {{link.journal}}</em>
      </div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <button class="bibtex" role="button" target="_blank" style="font-size:12px;" onclick="copyToClipboard(`{{ link.bibtex }}`)">BibTex</button>
      <!-- <a class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a> -->
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
<br>

{% assign counter = counter | plus: 1 %}
{% endif %}
{% endfor %}
</ol>
</div>

<!-- Conferences Section -->
<h3 class="conference" style="margin: 20px 0px -20px 20px; font-size: 20px">Conferences</h3>
<div class="publications">
<ol class="bibliography">
{% assign counter = 1 %}
{% for link in site.data.publications.main %}
{% if link.type == "2" %}
<li>
<div class="pub-row">
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><span>{{ counter }}. </span><a href="{{ link.doi }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference}} {{link.journal}}</em>
      </div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <button class="bibtex" role="button" target="_blank" style="font-size:12px;" onclick="copyToClipboard(`{{ link.bibtex }}`)">BibTex</button>
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
<br>

{% assign counter = counter | plus: 1 %}
{% endif %}
{% endfor %}
</ol>
</div>

