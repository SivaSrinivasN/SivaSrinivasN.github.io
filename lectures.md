---
layout: default
title: Lectures
permalink: /lectures/
lectures:
  - title: Introduction to Network Optimization
    date: ""
    pdf: /uploads/lectures/network-optimization.pdf
  - title: Machine Learning Fundamentals
    date: ""
    pdf: /uploads/lectures/machine-learning-fundamentals.pdf
  - title: GPU Computing and Energy Efficiency
    date: ""
    pdf: /uploads/lectures/gpu-computing.pdf
---

<div class="lecture-page">
    <h1>Lecture Notes &amp; Study Plan</h1>

    <section aria-labelledby="lectures-heading">
        <h2 id="lectures-heading">Lectures</h2>
        <ul class="lecture-list">
            {% for lecture in page.lectures %}
            {% assign pdf_file = site.static_files | where: 'path', lecture.pdf | first %}
            <li>
                {% if lecture.date != empty %}<span>{{ lecture.date | escape }}:</span>{% endif %}
                <span>Lecture-{% if forloop.index < 10 %}0{% endif %}{{ forloop.index }}</span>
                {% if pdf_file %}
                <a href="{{ lecture.pdf | relative_url | escape }}" target="_blank" rel="noopener" aria-label="{{ lecture.title | escape }} (PDF, opens in a new tab)">{{ lecture.title | escape }}</a>
                {% else %}
                <span>{{ lecture.title | escape }}</span> <span class="lecture-status">(notes coming soon)</span>
                {% endif %}
            </li>
            {% endfor %}
        </ul>
    </section>

    <section aria-labelledby="study-topics-heading">
        <h2 id="study-topics-heading">Study Topics</h2>
        <ul>
            <li>Network optimization</li>
            <li>Machine learning fundamentals</li>
            <li>GPU computing and energy efficiency</li>
        </ul>
    </section>

    <section aria-labelledby="description-heading">
        <h2 id="description-heading">Description</h2>
        <p>A collection of my study notes, organized in the order I plan to study the topics. Available notes are linked in blue and open as PDFs in a new tab.</p>
    </section>
</div>

{% comment %}
To add a lecture, append an entry to the lectures list at the top of this file:
  - title: Your lecture title
    date: "21 Sep 2026"
    pdf: /uploads/lectures/your-notes.pdf

Upload the PDF at that exact path, including matching capitalization.
The title becomes a blue link automatically when the PDF exists.
Leave date as "" to omit it. Lecture numbers follow the list order.
{% endcomment %}
