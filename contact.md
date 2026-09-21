---
layout: default
title: Contact
permalink: /contact/
---

# Contact Information

**Email:** sivasrinivas@iisc.ac.in  
**Department:** Electrical Communication Engineering  
**Institute:** Indian Institute of Science, Bangalore

## Office:
ECE Department, IISc Bangalore

{% if site.social_links.google_scholar != empty or site.social_links.linkedin != empty %}
<div class="social-links" role="group" aria-label="Academic and social profiles">
    {% if site.social_links.google_scholar != empty %}
    <a href="{{ site.social_links.google_scholar | escape }}" aria-label="Google Scholar profile" title="Google Scholar">
        <svg width="18" height="18" viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path fill="currentColor" d="M12 1 0 9l4 2.67V19h2v-6l6 4 12-8L12 1Zm-5 15v4c3 3 7 3 10 0v-4l-5 3.33L7 16Z"/></svg>
    </a>
    {% endif %}
    {% if site.social_links.linkedin != empty %}
    <a href="{{ site.social_links.linkedin | escape }}" aria-label="LinkedIn profile" title="LinkedIn">
        <svg width="18" height="18" viewBox="0 0 24 24" aria-hidden="true" focusable="false"><rect width="24" height="24" rx="3" fill="currentColor"/><path fill="var(--section-bg)" d="M5 9h3v10H5V9Zm1.5-5a1.75 1.75 0 1 0 0 3.5 1.75 1.75 0 0 0 0-3.5ZM10 9h3v1.4c.7-1.1 1.7-1.7 3-1.7 2.6 0 3.5 1.6 3.5 4.4V19h-3v-5.2c0-1.5-.3-2.5-1.7-2.5-1.5 0-1.8 1.2-1.8 2.5V19h-3V9Z"/></svg>
    </a>
    {% endif %}
</div>
{% endif %}
