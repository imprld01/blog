---
layout	: default
title	: 心情雜記
---

<article id="main">
    <header class="special container">
        <span class="icon fa-moon-o"></span>
        <h2><a href="{{ site.baseurl }}">&lt;{{ page.title }}&gt;</a></h2>
    </header>
    <section class="wrapper style4 container">
        <ul class="posts">
          {% for post in site.categories.mood-essey %}
            <li class="wrapper {% if forloop.first %} style2 {% else %} style1 {% endif %}">
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