---
layout: page
title: research
permalink: /research/
description: 
nav: true
nav_order: 2
display_categories: 
horizontal: false
---

{% assign course_items = site.research | sort: 'none' | reverse %}

{% for item in research_items %}
  <h3>{{ item.title }}</h3>
  <p>{{ item.content }}</p>
{% endfor %}
