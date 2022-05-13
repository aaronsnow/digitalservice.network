---
layout: home
show_excerpts: false
---

## Welcome
- [Sign up to join our mailing list](https://airtable.com/shrltywvcMrfvKbpN).
- We're building a [library]({{ site.baseurl }}/library), starting with a collection of [job descriptions]({{ site.baseurl }}/library/job-descriptions) for digital roles in government from several different governments.

{% assign latest = site.posts.first %}
## The latest: [{{ latest.title | escape }}]({{ latest.url | relative_url }})

_(Click [here]({{ site.baseurl }}/updates) to see all our updates.)_

{% unless page.show_excerpts == false %}
{{ latest.excerpt }}
{% if latest.content.size > latest.excerpt.size %}... [\[continue reading\]]({{latest.url | relative_url }}){% endif %}
{% else %}
{{ latest.content }}
{% endunless %}
