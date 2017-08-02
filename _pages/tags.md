---
layout: page
title: Tags
permalink: /tags/
custom_css: tags
---

Click on a tag to see relevant list of posts:
<br>

{% for tag in site.tags %}
  {% assign t = tag | first %}
  [`{{ t | downcase }}`]({{ site.url }}/tags/#{{ t | downcase | replace:" ","-" }}) 
{% endfor %}

---

{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}

<h4><a name="{{ t | downcase | replace:" ","-" }}"></a><a class="internal" href="/tag/#{{ t | downcase | replace:" ","-" }}">{{ t | downcase }}</a></h4>
<ul>
{% for post in posts %}
  {% if post.tags contains t %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="date">{{ post.date | date: "%B %-d, %Y"  }}</span>
  </li>
  {% endif %}
{% endfor %}
</ul>

---

{% endfor %}
