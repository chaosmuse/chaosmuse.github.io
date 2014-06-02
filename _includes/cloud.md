<h3>Categories</h3>
<span>
	{% for category in site.categories %}
		<li style="font-size: {{ category | last | size | times: 100 | divided_by: site.categories.size | plus: 30 }}%">
			<a href="/{{ site.category_dir }}/{{ category | first }}/">{{ category | first }}</a>
		</li>
	{% endfor %}
</span>