---
title: Posts By Category
layout: default

---

<h1>{{ page.title }}</h1>

{% for category in site.categories %}
<h2 class="cat-list">{{ category | first | capitalize }}</h2>

{% for posts in category %}
{% for post in posts %}
{% if post.url %}
{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
{% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}
{% if forloop.first %}
<h3 class="cat-year">{{this_year}}</h3>
<ul class="cat-year-items">
{% endif %}
{% if forloop.last %}
</ul>
{% else %}
{% if this_year != next_year %}
</ul>
<h3 id="cat-year">{{next_year}}</h2>
<ul class="cat-year-items">
{% endif %}
{% endif %}

<li class="cat-year-item"><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endif %}

{% endfor %}
{% endfor %}

{% endfor %}
