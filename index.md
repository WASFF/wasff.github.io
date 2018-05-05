title: WASFF Demo Site
description: Github Pages Demonstration
---

## Collections
{% for collection in site.collections %}
{{ collection.directory }}">{{ collection }}
Label: {{ collection.label }}

{% endfor %}


## Minutes
<ul>
{% for item in site.minutesindexs %}
<li> <a href="{{ item.path }}" {{ item.name }} </a>
{% endfor %}
</ul>


