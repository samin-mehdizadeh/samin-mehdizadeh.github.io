<h2 id="research-experiences" style="margin: 2px 0px -15px;">Research Experiences</h2>

<div class="publications research-experiences">
<ol class="bibliography">

{% for item in site.data.research_experiences.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if item.image %}
    <img src="{{ item.image }}" class="research-logo z-depth-1">
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title">{% if item.link %}<a href="{{ item.link }}">{{ item.name }}</a>{% else %}{{ item.name }}{% endif %}</div>
      {% if item.role %}<div class="author">{{ item.role }}</div>{% endif %}
      {% if item.period %}<div class="periodical"><em>{{ item.period }}</em></div>{% endif %}
      {% if item.description %}<div class="description" style="margin-top:0.5rem;font-size:0.95rem;line-height:1.5;color:var(--global-text-color);">{{ item.description }}</div>{% endif %}
    <div class="links">
      {% if item.link %}
      <a href="{{ item.link }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Website</a>
      {% endif %}
      {% if item.advisor %}
      <span style="font-size:12px;">Advisor: {% if item.advisor_link %}<a href="{{ item.advisor_link }}" target="_blank">{{ item.advisor }}</a>{% else %}{{ item.advisor }}{% endif %}</span>
      {% endif %}
      {% if item.notes %}
      <strong> <i style="color:#e74d3c">{{ item.notes }}</i></strong>
      {% endif %}
      {% if item.others %}
      {{ item.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
