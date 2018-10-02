---
title: "INT 5: Data Science Foundations, Fall 2018"
---

<div class="container">
<section id="content">
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

<div class="calendar">
<table class="table table-sm">
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
{% if item.links.demo %}[Demo]({{item.links.demo}}){% endif %}  
{% if item.links.slides %}[Slides]({{item.links.slides}}){% endif %}  
{% if item.links.video %}[Video]({{item.links.video}}){% endif %}  
</td>
<td markdown="1">
{% for reading in item.readings %}[{{reading.title}}]({{reading.url}})<br/>{% endfor %}
</td>
<td markdown="1">
{% for asn in item.assignments %}[{{asn.title}}]({{asn.url}})<br/>{% endfor %}
</td>
</tr>
{% endfor %}
</tbody>
</table>
</div> <!--end calendar -->
</div>
</section>
</div> <!--end container -->
