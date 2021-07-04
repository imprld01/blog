---
layout	: default
title	: Tag Cloud
---

<article id="main">
	<header class="special container">
		<span class="icon fa-cloud"></span>
		<h2 class="post-title">&lt;{{ page.title }}&gt;</h2>
	</header>

	<section class="style4 wrapper container">
		<ul style="display: inline">
			{% assign sorted_tags = (site.tags | sort: 0) %}
			{% for tag in sorted_tags %}
				<li style="display: inline;font-size: {{ tag | last | size | times: 100 | divided_by: site.tags.size | plus: 35  }}%">
					<a href="{{ site.baseurl }}/tag-cloud/Tag-{{ tag[0] }}">
						{{ tag | first }} ({{ tag | last | size }})
					</a>
				</li>&nbsp;
			{% endfor %}
		</ul>
	</section>
</article>