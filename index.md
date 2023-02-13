---
layout: default
---

<h1>Latest Blog</h1>

<h2>{{ page.posts[0].title }}</h2>
<p>{{ page.posts[0].excerpt }}</p>
<a href="{{ page.posts[0].url }}">Read More</a>

<h1>Previous 3 Blogs</h1>

<ul>
{% for post in page.posts limit:3 offset:1 %}
  <li>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt }}</p>
  </li>
{% endfor %}
</ul>

