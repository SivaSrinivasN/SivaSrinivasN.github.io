---
layout: default
title: Home
---

<!-- Profile picture and About side by side -->
<section class="profile-about-section">
    <img src="/Srinivas.jpeg" alt="Srinivas Nomula" class="profile-picture">
    <div class="about-content">
        <h1>Srinivas Nomula</h1>
        <p class="designation">PhD Student | <a href="https://iisc.ac.in/">Indian Institute of Science</a></p>
        <div class="bio">
            <p>Hello! I'm a 4th year PhD student in the ECE Dept., IISc, advised by <a href="https://ece.iisc.ac.in/~parimal/"> Prof. Parimal Parag</a>. I'm interested to work on Networking, Machine learning and GPU energy minimization.</p>
            <p>My research focuses on developing efficient algorithms for network optimization and energy-aware computing systems.</p>
        </div>
    </div>
</section>

<!-- News & Updates section -->
<section class="news-section">
    <h2>News & Updates</h2>
    
    {% for post in site.posts limit:5 %}
    <div class="news-item">
        <div class="news-date">{{ post.date | date: "%b %Y" }}</div>
        <div class="news-content">
            {{ post.content }}
        </div>
    </div>
    {% endfor %}
</section>