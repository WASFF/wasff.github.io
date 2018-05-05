---
title: WASFF Demo Site
description: Github Pages Demonstration
---



## Minutes
{% assign thisyear = 'now' | date: "%Y" %}
<ul>
  {% for item in site.minutesindexs %}  
    {% capture yearsago %}{{ item.title | minus: thisyear }}{% endcapture %}
    <!-- If the number of years ago is negative, then itis in the future so do notshow it -->
    {% unless yearsago contains '-' %}
      <li> <a href="{{ item.path }}" {{ item.name }} </a>
    {% endunless %}  
  {% endfor %}
</ul>


