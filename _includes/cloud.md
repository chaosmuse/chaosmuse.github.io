<h3><a href="/categories/">Categories</a></h3>
<span>
	{% for category in site.categories %}
	{% capture cat_size %}{{ category | last | size | times: 100 | divided_by: site.categories.size | plus: 35 }}{% endcapture %}
		<li style="font-size: {{cat_size}}%">
			{{ category | first }}
		</li>
	{% endfor %}
</span>