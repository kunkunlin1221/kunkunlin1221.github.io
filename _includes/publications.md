<h2 id="publications">Publications</h2>

<div class="publications">
<ol class="bibliography">
{% for item in site.data.publications.main %}
{% include entry.html item=item title_href=item.pdf %}
{% endfor %}
</ol>
</div>
