---
title: Programme 
permalink: /programme/

layout: page
---

{%- assign abs_url = '/assets/abstracts/pdf/' %} 
{%- assign all_talks = site.data.talks.accepted | concat: site.data.talks.invited %}

**Note**: all coffee breaks and the lunch on the first day are offered by the organisation 

<br> 

<table>
  <tbody> 
{%- for d in site.data.schedule23 %}
<tr> <th colspan="2"> {{ d.day }} </th> </tr> 
{%- for slot in d.slots %}
{%- if slot.type == "talk" %} 
{%- assign talks = all_talks | where_exp: "item", "item.slot == slot.id" %} 
{%- for t in talks %} 
<tr>
  <td> {{ slot.time }} </td>
  <td> 
    <a href="{{ t.abs | prepend: abs_url | relative_url }}" target="_blank">{{ t.author }}</a> 
  </td>
</tr> 
{%- endfor %} 
{%- else %}
<tr>
  <td> <strong>{{ slot.time }}</strong> </td>
  <td> <strong>{{ slot.type }}</strong> </td>
</tr> 
{%- endif %} 
{%- endfor %} 
{% endfor %} 
</tbody> </table> 




