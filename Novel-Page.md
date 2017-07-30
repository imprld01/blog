---
layout: default
---

<article id="main">
    <header class="special container">
        <span class="icon fa-book"></span>
        <h2><a href="/blog">&lt;御風翱翔．知識漫遊&gt;</a></h2>
    </header>
    <section class="wrapper style4 container">
        <ul class="posts">
          {% for post in site.categories.novel %}
            <li class="wrapper {% if forloop.first %} style2 {% else %} style1 {% endif %}">
              <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
                {{ post.excerpt }}
                <section class="special">
                    <ul class="buttons">
                        <li><a href="{{ post.url }}" class="button">Read more</a></li>
                    </ul></section>
            </li>
          {% endfor %}
        </ul>
    </section>
</article>