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

{% if site.enable_research_categories and page.display_categories %} {% for category in page.display_categories %}

{{ category }}

{% assign categorized_research = site.research | where: "category", category %} {% assign sorted_research = categorized_research | sort: "importance" %} {% if page.horizontal %}
{% for research in sorted_research %} {% include research_horizontal.liquid %} {% endfor %}
{% else %}
{% for research in sorted_research %} {% include research.liquid %} {% endfor %}
{% endif %} {% endfor %}
{% else %}

{% assign sorted_research = site.research | sort: "importance" %}

{% if page.horizontal %}

{% for research in sorted_research %} {% include research_horizontal.liquid %} {% endfor %}
{% else %}
{% for research in sorted_researchs %} {% include research.liquid %} {% endfor %}
{% endif %} {% endif %}
