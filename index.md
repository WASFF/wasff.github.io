---
title: WASFF Demo Site
description: Github Pages Demonstration
---



## Minutes

{% assign thisyear = 'now' | date: "%Y" %}
{% for item in site.minutesindexs %}  
  {% capture yearsago %}{{ thisyear | minus: item.title }}{% endcapture %}
  <!-- If the number of years ago is negative, then itis in the future so do notshow it -->
  {% unless yearsago contains '-' %}
    - [{{ item.name }}]({{ item.url }}) 
  {% endunless %}  
{% endfor %}

 


