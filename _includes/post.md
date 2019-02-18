<div class="post">
	<h2 class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></h2>
	<h3 class="post-date">{{ post.date | date_to_string }}</h3>
	<span>{{ post.content }}</span>
	<span>Posted under {{ post.categories  join: ',' }}</span>
</div>
