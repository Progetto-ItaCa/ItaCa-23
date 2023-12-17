---
title: Participants
permalink: /Participants/

layout: page
---

{% assign ps = site.data.participants  %}

{% for p in ps %}
{% if p.affiliation %}
* {{p.name}} {{p.surname}} ({{p.affiliation}})
{% else %}
* {{p.name}} {{p.surname}}
{% endif %}
{% endfor %}
