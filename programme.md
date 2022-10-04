---
title: Programme 
permalink: /programme/

layout: page
---

<!-- {%- assign abs_url = '/assets/abstracts/' %} 
{%- assign talks = site.data.talks | sort: 'slot' %} 

<table>
  <tbody> 
{% for t in talks %} 
{% if t.slot == "1a" %}
<tr> <th colspan="2">  Monday 20 December </th> </tr> 
<tr> <td> 13.00 - 13.25 </td> <td><strong>registration</strong></td> </tr> 
<tr> <td> 13.25 - 13.30 </td> <td><strong>opening</strong></td> </tr> 
{% endif %}
{% if t.slot == "4a" %}
<tr> <th colspan="2"> Tuesday 21 December </th> </tr> 
<tr> <td> 08.45 - 09.00 </td> <td><strong>registration</strong></td> </tr> 
{% endif %} 
<tr>
  <td> {{ t.time }} </td>
  <td> 
    <a href="{{ t.abs | prepend: abs_url | relative_url }}" target="_blank">{{ t.author }}</a> 
  </td>
</tr> 
{%- if t.slot == "1c" %}
<tr> 
  <td> 15.00 - 15.30 </td>
  <td> <strong>coffee break</strong> </td>
</tr> 
{% endif -%} 
{%- if t.slot == "2c" %}
<tr>
  <td> 17.00 - 17.30 </td>
  <td> <strong>coffee break</strong> </td>
</tr>
{% endif -%} 
{%- if t.slot == "4c" %}
<tr>
  <td> 10.30 - 11.00 </td>
  <td> <strong>coffee break</strong> </td> 
</tr>
{% endif -%} 
{%- if t.slot == "5c" %}
<tr>
  <td> 12.30 - 14.00 </td>
  <td> <strong>lunch break</strong> </td>
</tr> 
{% endif -%} 
{% endfor %} 
</tbody> </table> 

**Note**: only coffee breaks are offered by the workshop organisation. Suggestions for lunch can be found [here]({{ '/venue/' | relative_url }}).


 -->

