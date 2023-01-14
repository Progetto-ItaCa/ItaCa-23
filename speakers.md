---
title: Speakers 
permalink: /speakers/

layout: page
---

{%- if site.data.talks.invited -%}
## Invited Talks 
{% for t in site.data.talks.invited %}
{% if t.url %}
[{{ t.author }}]({{ t.url }}) ({{ t.affiliation }})  
{% else %}
{{ t.author }} ({{ t.affiliation }})  
{% endif -%}  
**{{ t.title }}** <br/> 
{%- if t.abs %}
[abstract]({{ t.abs | prepend: '/assets/abstracts/' | relative_url }}){:target="_blank"}
{% if t.slides %} • [slides]({{ t.slides | prepend: '/assets/slides/' | relative_url }}){:target="_blank"} {% endif -%} 
{% if t.video %} • [video]({{ t.video }}){:target="_blank"} {% endif %} 
{% endif %}

{% endfor %}
{%- endif -%}


{%- if site.data.talks.accepted -%}
## Contributed Talks 
{% for t in site.data.talks.accepted %}
{% if t.url %}
[{{ t.author }}]({{ t.url }}) ({{ t.affiliation }})  
{% else %}
{{ t.author }} ({{ t.affiliation }})  
{% endif -%}  
**{{ t.title }}** <br/> 
{%- if t.abs %}
[abstract]({{ t.abs | prepend: '/assets/abstracts/' | relative_url }}){:target="_blank"}
{% if t.slides %} • [slides]({{ t.slides | prepend: '/assets/slides/' | relative_url }}){:target="_blank"} {% endif -%} 
{% if t.video %} • [video]({{ t.video }}){:target="_blank"} {% endif %} 
{% endif %}

{% endfor %}
{%- endif -%}
