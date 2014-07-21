<h3><a href="/categories/">Categories</a></h3>
<span>
	{% for category in site.categories %}
		<li style="font-size: {{ category | last | size | times: 100 | divided_by: site.categories.size | plus: 30 }}%">
			{{ category | first }}
		</li>
	{% endfor %}
</span>