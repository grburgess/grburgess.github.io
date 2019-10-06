---
title: Blog
layout: single
permalink: /blog/
---
I occasionally have things to say.

<!-- <ul> -->
<!--   {% for post in site.categories.blog %} -->
<!-- 	<li> -->
<!--       <a href="{{ post.url }}">{{ post.title }}</a> -->
<!--     </li> -->

<!--   {% endfor %} -->
<!-- </ul> -->

{% for post in site.posts %}
<div class="row">
	<div class="small-12 columns">
  	
	 {% if post.category != 'science'  %}	
		<sub>{{ post.date | date: '%B %d, %Y' }}</sub>
		<a href="{{ post.url }}"><h3>{{ post.title }}</h3></a>

	  	{{ post.excerpt }}

		<ul class="inline-list" style="margin-top:-1em;">
			{% for category in post.categories %}
			<li><h6><a href="/#!/{{ category }}"><i class="fa fa-tag"></i> {{ category }}</a></h6></li>
			{% endfor %}
		</ul>
	{% endif %}

	</div>
</div>
{% endfor %}
