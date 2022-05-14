---
layout: home
show_excerpts: true
latest_count: 2
---

## Welcome
- [Sign up to join our mailing list](https://airtable.com/shrltywvcMrfvKbpN).
- We're building a [library]({{ site.baseurl }}/library), starting with a collection of [job descriptions]({{ site.baseurl }}/library/job-descriptions) for digital roles in government from several different governments.

## Recent Updates

<div class="home-recent-updates-wrapper">
{% for latest in site.posts limit:page.latest_count %}

<div class="home-recent-updates">
<h3><a href="{{ latest.url | relative_url }}">{{ latest.title | escape }}</a></h3>
    {% unless page.show_excerpts == false %}
{{ latest.excerpt }}
        {% if latest.content.size > latest.excerpt.size %} 
<a href="{{latest.url | relative_url }}">[continue reading "{{ latest.title | truncatewords: 4 }}"]</a>
        {% endif %}
    {% else %}
{{ latest.content }}
    {% endunless %}
</div><!-- home-recent-updates -->
{% endfor %}
</div><!-- home-recent-updates-wrapper -->
### [⇨ All updates]({{ site.baseurl }}/updates)