---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

{% assign groups = site.elecciones | group_by: "tipo" | sort: "fecha" %}

{% for group in groups %}
    {{ group.name }}
    {% for item in group.items %}
        {{item.pais}}
    {%endfor%}
{%endfor%}
