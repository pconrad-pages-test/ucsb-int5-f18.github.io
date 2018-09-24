---
title: "INT 5: Data Science Foundations, Fall 2018"
---

<!--# {{site.course}}, {{site.quarter}}-->


<div id="info">
<h2>Course Information</h2>
<ul>
{% for item in site.info %}
<li><a href="{{item.url}}">{{item.title}}</a></li>
{% endfor %}
</ul>
</div>

<div id="info">
<h2>Lectures</h2>

<table>
<thead>
<tr>
<td class="header">Date</td>
<td class="header">Topic</td>
<td class="header">Lecture</td>
<td class="header">Reading</td>
<td class="header">Assignment</td>
</tr>
</thead>

<tbody>
{% for item in site.lectures %}
<tr>
  <td markdown="1">
{{ item.date | date: "%a %m/%d"  }}
  </td>
    <td markdown="1">
      {{ item.topic }}
  </td>
    <td markdown="1">
      {% if item.links.demo %}[Demo]({{item.links.demo}}){% endif %}, TODO, LIKEWISE FOR SLIDES/VIDEO 
  </td>
  <td markdown="1">
      {% for reading in item.readings %}
      [{{reading.title}}]({{reading.url}})&nbsp;
      {% endfor %}
  </td>
  <td markdown="1">
      {% for asn in item.assignments %}
      [{{asn.title}}]({{asn.url}})&nbsp;       {% endfor %}
  </td>
</tr>
{% endfor %}
</tbody>
</table>
</div>
