---
title: Programme 
permalink: /programme/

layout: page
---

To attend the workshop remotely, use the following links
* [21 December morning](https://www.youtube.com/watch?v=Z1SIYpMWWLU){:target="_blank"}
* [21 December afternoon](https://www.youtube.com/watch?v=9tJGqULK7tE){:target="_blank"}
* [22 December morning](https://www.youtube.com/watch?v=sTSuGLPKMC0){:target="_blank"}

{%- assign abs_url = '/assets/abstracts/' %} 

<table>
  <tbody> 
{%- for d in site.data.schedule %}
<tr> <th colspan="2"> {{ d.day }} </th> </tr> 
{%- for slot in d.slots %}
{%- if slot.type == "talk" %} 
{%- if slot.invited %} 
{%- assign talks = site.data.talks.invited | where_exp: "item", "item.slot == slot.id" %} 
{%- else %} 
{%- assign talks = site.data.talks.accepted | where_exp: "item", "item.slot == slot.id" %} 
{%- endif %}
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

**Note**: only coffee breaks are offered by the workshop organisation. Suggestions for lunch can be found [here]({{ '/venue/' | relative_url }}).



