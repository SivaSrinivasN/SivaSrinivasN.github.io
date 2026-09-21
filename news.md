---
layout: default
title: Past News
permalink: /news/
---

<section class="news-section" aria-labelledby="news-heading">
    <h1 id="news-heading">Past News</h1>
    <p class="news-intro">All updates, from newest to oldest.</p>
    {% assign updates = site.data.news | where_exp: "item", "item.date != ''" | sort: "date" | reverse %}
    {% for item in updates %}
        {% include news-item.html item=item %}
    {% else %}
        <p>No news yet.</p>
    {% endfor %}
</section>
<p class="news-navigation"><a href="{{ '/' | relative_url }}">Back to home</a></p>
