---
layout: page
title: class
tagline: Hopefully I learned something today...

---
{% include JB/setup %}


{% for post in site.posts limit:1 %}
<p>
    <a href="{{ post.url }}">
    <h3>{{ post.title }}</h3>
    </a>
    <p class="blogdate">{{ post.date | date: "%d %B %Y" }}</p>
    <div>{{ post.content |truncatehtml | truncatewords: 60 }}</div>
</p>
{% endfor %}
