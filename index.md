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
        {% if site.social_links.google_scholar != empty or site.social_links.linkedin != empty %}
        <div class="social-links" role="group" aria-label="Academic and social profiles">
            {% if site.social_links.google_scholar != empty %}
            <a href="{{ site.social_links.google_scholar | escape }}" aria-label="Google Scholar profile" title="Google Scholar">
                <svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path fill="currentColor" d="M12 1 0 9l4 2.67V19h2v-6l6 4 12-8L12 1Zm-5 15v4c3 3 7 3 10 0v-4l-5 3.33L7 16Z"/></svg>
            </a>
            {% endif %}
            {% if site.social_links.linkedin != empty %}
            <a href="{{ site.social_links.linkedin | escape }}" aria-label="LinkedIn profile" title="LinkedIn">
                <svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><rect width="24" height="24" rx="3" fill="currentColor"/><path fill="var(--section-bg)" d="M5 9h3v10H5V9Zm1.5-5a1.75 1.75 0 1 0 0 3.5 1.75 1.75 0 0 0 0-3.5ZM10 9h3v1.4c.7-1.1 1.7-1.7 3-1.7 2.6 0 3.5 1.6 3.5 4.4V19h-3v-5.2c0-1.5-.3-2.5-1.7-2.5-1.5 0-1.8 1.2-1.8 2.5V19h-3V9Z"/></svg>
            </a>
            {% endif %}
        </div>
        {% endif %}
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
