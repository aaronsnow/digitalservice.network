---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
show_excerpts: false
---

## Welcome
Paragraph(s) here about why this exists, what we're here to do, who we are.

## Listserv/Membership
[Sign up to join our listserv / network](https://airtable.com/shrltywvcMrfvKbpN)

## Library
We're building a [Library](/library). We have job descriptions.

{% assign latest = site.posts.first %}
## The latest: [{{ latest.title | escape }}]({{ latest.url | relative_url }})

_(Click [here](/updates) to see all our updates.)_

{% unless page.show_excerpts == false %}
{{ latest.excerpt }} ... [\[continue reading\]]({{latest.url | relative_url }})
{% else %}
{{ latest.content }}
{% endunless %}
