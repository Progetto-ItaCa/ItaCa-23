---
title: Participants
permalink: /Participants/

layout: page
---

![ItaCa participants]({{ '/assets/img/group.jpg' | relative_url }}) 

{% assign ps = site.data.participants | sort: 'surname' %} 

{% for p in ps %}
{% if p.affiliation %} 
* {{p.name}} {{p.surname}} ({{p.affiliation}}) 
{% else %}
* {{p.name}} {{p.surname}}  
{% endif %} 
{% endfor %}
