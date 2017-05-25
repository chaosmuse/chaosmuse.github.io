{% include header.md %}
	<body>
		<div class="templateholder">
			<div class="Layout16_header">
				<a href="{{site.baseurl}}">{{ site.name }}</a>
			</div>
			<div class="Layout16_1">
				<ul>
				{% for entry in site.navigation %}
				<li>
				<a href="{{entry.path}}">{{ entry.name }}</a>
				</li>
				{% endfor %}
				</ul>
			</div>
			<div class="Layout16_2"></div>
			<div class="Layout16_3">