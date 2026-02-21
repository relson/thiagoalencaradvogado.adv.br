---
layout: default
title: Blog
permalink: /blog
---

<div class="container">
    <div class="section-title">
        <h2>Blog Jurídico</h2>
        <div class="divider"></div>
        <p>Notícias, artigos e orientações sobre seus direitos.</p>
    </div>

    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 40px;">
        {% for post in site.posts %}
        <article class="feature-card" style="text-align: left; padding: 0; overflow: hidden; border-bottom: 5px solid var(--gold);">
            <div style="padding: 30px;">
                <p style="color: var(--gold); font-size: 0.8rem; font-weight: bold; text-transform: uppercase; margin-bottom: 10px;">{{ post.date | date: "%d/%m/%Y" }}</p>
                <h3 style="margin-top: 0;"><a href="{{ post.url }}" style="color: var(--dark-blue); text-decoration: none;">{{ post.title }}</a></h3>
                <p style="font-size: 0.95rem; color: #666;">{{ post.content | strip_html | truncatewords: 30 }}</p>
                <a href="{{ post.url }}" style="color: var(--gold); font-weight: bold; text-decoration: none; display: inline-block; margin-top: 15px;">LER ARTIGO COMPLETO →</a>
            </div>
        </article>
        {% endfor %}
    </div>
</div>
