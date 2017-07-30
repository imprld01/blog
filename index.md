---
layout: default
---

<article id="main">
    <header class="special container">
        <span class="icon fa-book"></span>
        <h2><a href="{{ site.baseurl }}">&lt;御風翱翔．知識漫遊&gt;</a></h2>
    </header>
    <section class="wrapper style4 container">
        <ul class="posts">
			<li class="wrapper style2">
				<h2 style="margin-bottom:0em"><a href="{{ post.url }}">{{ post.title }}</a></h2>
                <p>Posted By {% if post.author %}{{ post.author }}{% endif %}{% if post.meta %}{{ post.meta }}{% endif %} on {{ post.date | date: "%b %-d, %Y" }}</p>
				{{ post.excerpt }}
				<section class="special">
                    <ul class="buttons">
                        <li><a href="{{ site.baseurl }}{{ post.url }}" class="button">Read More</a></li>
                    </ul>
				</section>
            </li>
			{% for post in site.posts %}
				<li class="wrapper style1">
					<h2 style="margin-bottom:0em"><a href="{{ post.url }}">{{ post.title }}</a></h2>
					<p>Posted By {% if post.author %}{{ post.author }}{% endif %}{% if post.meta %}{{ post.meta }}{% endif %} on {{ post.date | date: "%b %-d, %Y" }}</p>
					{{ post.excerpt }}
					<section class="special">
						<ul class="buttons">
							<li><a href="{{ site.baseurl }}{{ post.url }}" class="button">Read More</a></li>
						</ul>
					</section>
				</li>
			{% endfor %}
        </ul>
    </section>
</article>