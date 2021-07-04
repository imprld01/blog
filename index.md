---
layout			: default
title			: BW's Blog
title-cn		: 御風翱翔．知識漫遊
comment-count	: true
---

<article id="main">
    <header class="special container">
        <span class="icon fa-book"></span>
        <h2><a href="{{ site.baseurl }}">&lt;{{ page.title-cn }}&gt;</a></h2>
    </header>
    <section class="wrapper style4 container">
        <ul class="posts">
			{% for post in site.categories.Top-Post %}
				<li class="wrapper style2">
					<h2 style="margin-bottom:0em"><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
					<p>Posted By {% if post.author %}<a href="{{ site.github_url }}" style="color:white" target="_blank">{{ post.author }}</a>{% endif %} on {{ post.date | date: "%b %-d, %Y" }}</p>
					<p>
						<span class="icon fa-tag">:</span>
						{% for tag in post.tags %}
							<a href="{{ site.baseurl }}/tag-cloud/Tag-{{ tag }}"><span style="border-radius:5px;background-color:#337ab7;color:white;padding:7px;">{{ tag }}</span></a>&nbsp;
						{% endfor %}
						<span class="icon fa-comment"></span>
						<a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}#disqus_thread" data-disqus-identifier="{{ post.url }}" style="color:white">Loading...</a>
					</p>
					{{ post.excerpt }}
					<section class="special">
						<ul class="buttons">
							<li><a href="{{ site.baseurl }}{{ post.url }}" class="button">Read More</a></li>
						</ul>
					</section>
				</li><hr style="border: 1px solid #ccc">
			{% endfor %}
			{% for post in site.posts %}
				{% unless post.categories contains 'Top-Post' %}
					<li class="wrapper style1">
						<h2 style="margin-bottom:0em"><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
						<p>Posted By {% if post.author %}<a href="{{ site.github_url }}" style="color:#7c8081" target="_blank">{{ post.author }}</a>{% endif %} on {{ post.date | date: "%b %-d, %Y" }}</p>
						<p>
							<span class="icon fa-tag">:</span>
							{% for tag in post.tags %}
								<a href="{{ site.baseurl }}/tag-cloud/Tag-{{ tag }}"><span style="border-radius:5px;background-color:#337ab7;color:white;padding:7px;">{{ tag }}</span></a>&nbsp;
							{% endfor %}
							<span class="icon fa-comment"></span>
							<a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}#disqus_thread" data-disqus-identifier="{{ post.url }}" style="color:#7c8081">Loading...</a>
						</p>
						{{ post.excerpt }}
						<section class="special">
							<ul class="buttons">
								<li><a href="{{ site.baseurl }}{{ post.url }}" class="button">Read More</a></li>
							</ul>
						</section>
					</li>
					{% unless forloop.last %}
						<hr style="border: 1px solid #ccc">
					{% endunless %}
				{% endunless %}
			{% endfor %}
        </ul>
    </section>
</article>
