<h2 id="projects">Projects</h2>

<div class="publications">
<ol class="bibliography">
{% for item in site.data.projects.main %}
{% include entry.html item=item title_href=item.code %}
{% endfor %}
</ol>
</div>
