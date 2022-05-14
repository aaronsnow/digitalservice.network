---
title: Updates
layout: page
hide_nav: true
show_read_time: false
---

<div class="home">
  {%- if site.posts.size > 0 -%}
    <!-- <h2 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h2> -->
    <ul class="post-list">
      {%- for post in site.posts -%}
      <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <span class="post-meta">{{ post.date | date: date_format }}
          {%- if site.read_time == true and page.show_read_time != false -%}
            &nbsp; ·&nbsp; {%- include read-time.html content=post.content -%} min read
          {%- endif -%}
        </span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        {%- if site.show_excerpts != false and page.show_excerpts != false -%}
          {{ post.excerpt }} 
          {%- if post.content.size > post.excerpt.size -%}
          <a href="{{post.url | relative_url }}">[continue reading "{{ post.title | truncatewords: 4 }}"] </a>
          {%- endif -%}
        {%- else -%}
          {{ post.content }}
        {%- endif -%}
      </li>
      {%- endfor -%}
    </ul>

    <!-- <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p> -->
  {%- endif -%}
</div>