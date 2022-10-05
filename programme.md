---
title: Programme 
permalink: /programme/

layout: page
---

{%- assign abs_url = '/assets/abstracts/' %} 
{%- assign sessions = site.data.schedule|  %} 

<table>
  <tbody> 
{% for s in sessions %} 
{{ s.start-code }} 
{% for slot in s.slots %}
{%- assign talks = site.data.talks | where_exp: "item", "item.slot == slot.id" %} 
{%- for t in talks %} 
<tr>
  <td> {{ slot.time }} </td>
  <td> 
    <a href="{{ t.abs | prepend: abs_url | relative_url }}" target="_blank">{{ t.author }}</a> 
  </td>
</tr> 
{% endfor %} 
{% endfor %} 
{{ s.end-code }} 
{% endfor %} 
</tbody> </table> 

**Note**: only coffee breaks are offered by the workshop organisation. Suggestions for lunch can be found [here]({{ '/venue/' | relative_url }}).



