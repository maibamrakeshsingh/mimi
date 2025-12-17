<h2 id="" style="margin: 2px 0px -15px;"></h2>

<div class="publications" style="border: 1px solid #ddd; padding: 20px; border-radius: 8px; background: #fafafa;">

  <ol class="bibliography">

    {% for link in site.data.publications.main %}

    <li>
      <div class="pub-row" style="margin-bottom: 20px;">

        <div class="col-sm-3 abbr" style="position: relative; padding-right: 15px; padding-left: 15px;">
          {% if link.image %}
          <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width:100%; height:auto;">
          {% if link.conference_short %}
          <abbr class="badge">{{ link.conference_short }}</abbr>
          {% endif %}
          {% endif %}
        </div>

        <div class="col-sm-9" style="position: relative; padding-right: 15px; padding-left: 20px;">
          <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
          <div class="author">{{ link.authors }}</div>
          <div class="periodical"><em>{{ link.conference }}</em></div>

          <div class="links" style="margin-top: 5px;">
            {% if link.pdf %}
            <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">PDF</a>
            {% endif %}

            {% if link.code %}
            <a href="{{ link.code }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">Code</a>
            {% endif %}

            {% if link.page %}
            <a href="{{ link.page }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">Project Page</a>
            {% endif %}

            {% if link.bibtex %}
            <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">BibTex</a>
            {% endif %}

            {% if link.notes %}
            <strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>
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
