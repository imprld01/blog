---
layout	: One-Tag
title	: Posts tagged by &lt;Announcement&gt;
tag		: Announcement
---

<article id="main">
	<header class="special container">
		<span class="icon fa-tag"></span>
		<h2 class="post-title">{{ page.title }}</h2>
	</header>

	<section class="style4 wrapper container">
		<ul>
			{% for post in site.posts %}
				{% for tag in post.tags %}
					{% if tag contains page.tag %}
						<li>
							<time style="color:#666;font-size:11px;" datetime='{{post.date | date: "%Y-%m-%d"}}'>{{post.date | date: "%m/%d/%y"}}</time> <a class="archive_list_article_link" href='{{ post.url }}'>{{ post.title }}</a>
							<p>{{ post.summary }}</p>
							<ul>
								{% for tag in post.tags %}
									<li><a href="{{ site.baseurl }}{{ page.categories }}/Tag-{{ tag }}">{{ tag }}</a></li>
								{% endfor %}
							</ul>
						</li>
					{% endif %}
				{% endfor %}
			{% endfor %}
		</ul>
	</section>
</article>