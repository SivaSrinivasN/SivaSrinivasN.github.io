---
layout: default
title: Contact
permalink: /contact/
---

# Contact Information

**Email:** sivasrinivas@iisc.ac.in  
**Department:** Electrical Communication Engineering  
**Institute:** Indian Institute of Science, Bangalore

{% if site.social_links %}
<div class="social-links" role="group" aria-label="Academic and social profiles">
    {% if site.social_links.google_scholar and site.social_links.google_scholar != empty %}
    <a href="{{ site.social_links.google_scholar | escape }}" aria-label="Google Scholar profile" title="Google Scholar">
        <svg width="18" height="18" viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path fill="currentColor" d="M12 1 0 9l4 2.67V19h2v-6l6 4 12-8L12 1Zm-5 15v4c3 3 7 3 10 0v-4l-5 3.33L7 16Z"/></svg>
    </a>
    {% endif %}
    {% if site.social_links.linkedin and site.social_links.linkedin != empty %}
    <a href="{{ site.social_links.linkedin | escape }}" aria-label="LinkedIn profile" title="LinkedIn">
        <svg width="18" height="18" viewBox="0 0 24 24" aria-hidden="true" focusable="false"><rect width="24" height="24" rx="3" fill="currentColor"/><path fill="var(--section-bg)" d="M5 9h3v10H5V9Zm1.5-5a1.75 1.75 0 1 0 0 3.5 1.75 1.75 0 0 0 0-3.5ZM10 9h3v1.4c.7-1.1 1.7-1.7 3-1.7 2.6 0 3.5 1.6 3.5 4.4V19h-3v-5.2c0-1.5-.3-2.5-1.7-2.5-1.5 0-1.8 1.2-1.8 2.5V19h-3V9Z"/></svg>
    </a>
    {% endif %}
    {% if site.social_links.orcid and site.social_links.orcid != empty %}
    <a href="{{ site.social_links.orcid | escape }}"
       aria-label="ORCID profile" title="ORCID">
        <svg width="18" height="18" viewBox="0 0 256 256"
            xmlns="http://www.w3.org/2000/svg"
            aria-hidden="true" focusable="false">
            <circle cx="128" cy="128" r="128" fill="#A6CE39"/>
            <g fill="#FFFFFF">
                <path d="M86.3,186.2H70.9V79.1h15.4v48.4V186.2z"/>
                <path d="M108.9,79.1h41.6c39.6,0,57,28.3,57,53.6c0,27.5-21.5,53.6-56.8,53.6h-41.8V79.1z M124.3,172.4h24.5c34.9,0,42.9-26.5,42.9-39.7c0-21.5-13.7-39.7-43.7-39.7h-23.7V172.4z"/>
                <path d="M88.7,56.8c0,5.5-4.5,10.1-10.1,10.1c-5.6,0-10.1-4.6-10.1-10.1c0-5.6,4.5-10.1,10.1-10.1C84.2,46.7,88.7,51.3,88.7,56.8z"/>
            </g>
        </svg>
    </a>
    {% endif %}
    {% if site.social_links.cv and site.social_links.cv != empty %}
    <a href="{{ site.social_links.cv | relative_url | escape }}"
       target="_blank" rel="noopener"
       aria-label="Open CV (PDF, new tab)" title="CV (PDF)">
        <svg width="18" height="18" viewBox="0 0 24 24"
             fill="none" stroke="currentColor" stroke-width="1.5"
             stroke-linecap="round" stroke-linejoin="round"
             aria-hidden="true" focusable="false">
            <path d="M14 2H5v20h14V7z"/>
            <path d="M14 2v5h5M8 12h8M8 16h8"/>
        </svg>
    </a>
    {% endif %}
</div>
{% endif %}

## Office:
ECE Department, IISc Bangalore
