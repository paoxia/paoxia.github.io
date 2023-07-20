---
layout: page
title: Categories
permalink: /categories/
---
{% comment %}
==============
This is to make the categories sorted by their name.
site.categories[0]: tag name
site.categories[1]: array of posts in this tag
==============
{% endcomment %}
{% assign ordered_categories = site.categories | sort %}
{% for category in ordered_categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}