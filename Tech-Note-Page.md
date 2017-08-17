---
layout	: default
title	: 技術筆記
---

<article id="main">
    <header class="special container">
        <span class="icon fa-television"></span>
        <h2><a href="{{ site.baseurl }}">&lt;{{ page.title }}&gt;</a></h2>
    </header>
    <section class="wrapper style4 container">
        <ul class="posts">
          {% for post in site.categories.tech-note %}
            <li class="wrapper style1">
				<h2 style="margin-bottom:0em"><a href="{{ post.url }}">{{ post.title }}</a></h2>
                <p>Posted By {% if post.author %}<a href="{{ site.github_url }}" style="color:#7c8081" target="_blank">{{ post.author }}</a>{% endif %} on {{ post.date | date: "%b %-d, %Y" }}</p>
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