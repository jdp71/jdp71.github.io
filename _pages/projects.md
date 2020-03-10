---
layout: archive
permalink: /projects/
title: "Data Science Projects"
author_profile: true
header:
  image: ""
---


{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
