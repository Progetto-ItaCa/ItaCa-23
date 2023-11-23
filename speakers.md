---
title: Speakers 
permalink: /speakers/

layout: page
---

{%- if site.data.talks.invited -%}
## Invited Talks 
{% for t in site.data.talks.invited %}
{%- include talk %}
{% endfor %}
{%- endif -%}


{%- if site.data.talks.accepted -%}
## Contributed Talks 
{% for t in site.data.talks.accepted %}
{%- include talk %} 
{% endfor %}
{%- endif -%}
