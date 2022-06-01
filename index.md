---
layout: home
show_excerpts: true
latest_count: 2
---

> _“The most valuable thing about the digital service network is that it’s a group of people who are engaged in making digital happen. It’s experienced practitioners being open, supportive, and sharing successes and challenges. There’s no other network like it and although it’s new, I view it as a critical building block for the future of digital local government.” - former [sfgov](https://sf.gov) CDSO [Carrie Bishop](https://twitter.com/carriebish)_

# Welcome
This network is of public servants, for public servants, supported by the [Beeck Center](https://beeckcenter.georgetown.edu) and [U.S. Digital Response](https://usdigitalresponse.org). We've started to build a [library]({{ site.baseurl }}/library), beginning with a collection of [job descriptions]({{ site.baseurl }}/library/job-descriptions) for digital roles in government from several different governments. We're also busy planning events, helping transition teams and new administrations with government digitalization, advocating on behalf of digital service teams and efforts, and more.

You can [sign up here to join our mailing list]({{ site.baseurl }}/join). You can also find us on [Twitter](https://twitter.com/beeckcenter) or [LinkedIn](https://www.linkedin.com/company/beeckcenter/), or [send us an email](mailto:hi@digitalservice.network?Subject=Hi). We'd love to hear from you.

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