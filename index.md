---
layout: default
title: "Srinivas Nomula - Personal Website"
---

<section class="profile-about-section">
    <img src="{{ '/assets/images/Srinivas.jpeg' | relative_url }}" alt="Srinivas Nomula" class="profile-picture">
    <div class="about-content">
        <h1>Srinivas Nomula</h1>
        <p class="designation">PhD Student | <a href="https://iisc.ac.in/">Indian Institute of Science</a></p>
        <div class="bio">
            <p>Hello! I'm a 5th year PhD student in the ECE Dept., IISc. I'm interested to work on Networking, Machine learning and GPU energy minimization.</p>
            <p>My research focuses on analyzing, and modeling the stochasticity of systems in real time and provide necessary guarantees.</p>
        </div>
    </div>
</section>

<section class="news-section">
    <h2>News & Updates</h2>
    {% assign updates = site.data.news | where_exp: "item", "item.date != ''" | sort: "date" | reverse %}
    {% for item in updates limit:10 %}
        {% include news-item.html item=item %}
    {% else %}
        <p>No news yet.</p>
    {% endfor %}
    {% if updates.size > 10 %}
    <p class="news-navigation"><a class="past-news-button" href="{{ '/news/' | relative_url }}">Past news</a></p>
    {% endif %}
</section>
