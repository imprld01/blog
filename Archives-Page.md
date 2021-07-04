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
					{% unless post.next %}
						<div class="month" style="margin-left: 2em;">{{ post.date | date:"%b" }}</div>
					{% else %}
						{% capture month %}{{ post.date | date:"%b" }}{% endcapture %}
						{% capture nmonth %}{{ post.next.date | date:"%b" }}{% endcapture %}
						{% if month != nmonth %}
							<div class="month" style="margin-left: 2em;">{{ post.date | date:"%b" }}</div>
						{% endif %}
					{% endunless %}
					<div class="archive-post-title" style="margin-left: 4em;"><a style="font-weight: bold;" href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></div>
				</li>
			{% endfor %}
		</ul>
	</section>
</article>

