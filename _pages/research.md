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

<img src="/assets/img/research.png" alt="Research" width="800" height="400" style="float: center; margin-left: auto; margin-right: auto; margin-top: 50px; margin-bottom: 10px;">


{% assign research_items = site.research}

{% for item in research_items %}
  <h3>{{ item.title }}</h3>
  <p>{{ item.content }}</p>
{% endfor %}
