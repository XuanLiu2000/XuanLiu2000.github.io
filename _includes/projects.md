<style>

.no-list {
  list-style-type: none; 
  padding-left: 0;
}

.no-list li {
  margin-bottom: 10px; 
}

.custom-list {
  padding-left: 20px;
  list-style-type: disc;
  margin-top: 0;
  margin-bottom: 0;
  line-height: 1.5;
}

.custom-list li {
  margin-bottom: 5px;
  word-wrap: break-word;
}
</style>

<h4 style="margin:0 10px 0;">Projects</h4>

{% for link in site.data.projects.main %}
<li class="no-list">
  <div class="pub-row">
    <div class="col-sm-3 abbr" style="position: relative; padding-right: 15px; padding-left: 15px;">
        {% if link.image %}
        <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 250px; height: auto;">
        {% endif %}
    </div>
    <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
         <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
        <div class="work">
                {% if link.work %}
                <ul class="custom-list">
                  {% for point in link.work %}
                  <li>{{ point }}</li>
                  {% endfor %}
                </ul>
                {% endif %}
        </div>
        <div class="periodical"><em>{{ link.conference }}</em></div>
    </div>
  </div>
</li>
<br>
{% endfor %}


