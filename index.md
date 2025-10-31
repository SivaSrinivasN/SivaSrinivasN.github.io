<!-- ---
layout: default
title: Home
--- -->

<!-- Profile picture and About side by side -->
<!-- <section class="profile-about-section">
    <img src="/Srinivas.jpeg" alt="Srinivas Nomula" class="profile-picture">
    <div class="about-content">
        <h1>Srinivas Nomula</h1>
        <p class="designation">PhD Student | <a href="https://iisc.ac.in/">Indian Institute of Science</a></p>
        <div class="bio">
            <p>Hello! I'm a 4th year PhD student in the ECE Dept., IISc, advised by <a href="https://ece.iisc.ac.in/~parimal/"> Prof. Parimal Parag</a>. I'm interested to work on Networking, Machine learning and GPU energy minimization.</p>
            <p>My research focuses on developing efficient algorithms for network optimization and energy-aware computing systems.</p>
        </div>
    </div>
</section> -->

<!-- News & Updates section -->
<!-- <section class="news-section">
    <h2>News & Updates</h2>
    
    {% for post in site.posts limit:5 %}
    <div class="news-item">
        <div class="news-date">{{ post.date | date: "%b %Y" }}</div>
        <div class="news-content">
            {{ post.content }}
        </div>
    </div>
    {% endfor %}
</section> -->

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
            <p>Hello! I'm a 4th year PhD student in the ECE Dept., IISc. I'm interested to work on Networking, Machine learning and GPU energy minimization.</p>
            <p>My research focuses on developing efficient algorithms for network optimization and energy-aware computing systems. I'm passionate about bridging the gap between theoretical computer science and practical applications.</p>
        </div>
    </div>
</section>

<section class="news-section">
    <h2>News & Updates</h2>
    
    <div class="news-item">
        <div class="news-date">Aug 2025</div>
        <div class="news-content">
            <p>Appointed as a TPC member at <a href="https://www.comsnets.org/index.html">COMSNETS 2026</a></p>
        </div>
    </div>
    
    <div class="news-item">
        <div class="news-date">Dec 2024</div>
        <div class="news-content">
            <p>Our work on the <a href="https://ece.iisc.ac.in/~parimal/papers/2025/infocom.pdf">power of two in large service marketplaces</a> was accepted at <a href="https://infocom2025.ieee-infocom.org/">IEEE INFOCOM 2025</a></p>
        </div>
    </div>
</section>