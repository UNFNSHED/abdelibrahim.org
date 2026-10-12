---
layout: default
---

# Hi, I'm Abdo.

I build companies and small things on the internet. This is a short paragraph about who you are, what you care about, and what you're working on right now.

You can find me on [GitHub](https://github.com/UNFNSHED), [X](https://x.com/), or reach me at [hello@unfnshed.com](mailto:hello@unfnshed.com).

## Companies

<ul class="list">
{% for c in site.data.companies %}
  <li>
    <a href="{{ c.url }}">{{ c.name }}</a> <span class="muted">— {{ c.role }}</span>
    <p>{{ c.description }}</p>
  </li>
{% endfor %}
</ul>

## Projects

<ul class="list">
{% for p in site.data.projects %}
  <li>
    <a href="{{ p.url }}">{{ p.name }}</a> <span class="muted">{{ p.year }}</span>
    <p>{{ p.description }}</p>
  </li>
{% endfor %}
</ul>

## Writing

<ul class="posts">
{% for post in site.posts limit:5 %}
  <li><span class="muted">{{ post.date | date: '%Y-%m-%d' }}</span> <a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
<p><a href="{{ '/blog/' | relative_url }}">All posts →</a></p>
