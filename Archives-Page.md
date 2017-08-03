---
layout	: default
title	: Archives
---

<article id="main">
	<header class="special container">
		<span class="icon fa-archive"></span>
		<h2 class="post-title">&lt;{{ page.title }}&gt;</h2>
	</header>
	
	<section class="style4 wrapper container">	
		<ul>
			{% for post in site.posts %}
				{% unless post.next %}
					<h3>{{ post.date | date: '%Y' }}</h3>
				{% else %}
					{% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
					{% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
					{% if year != nyear %}
						<h3>{{ post.date | date: '%Y' }}</h3>
					{% endif %}
				{% endunless %}

				<li>    
					<div class="month" style="display: inline-block;">{{ post.date | date:"%b" }}</div>
					<div class="archive-post-title" style="display: inline-block;"><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></div>
				</li>
			{% endfor %}
		</ul>
	</section>
</article>

