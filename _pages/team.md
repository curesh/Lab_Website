---
title: "VMG - People"
layout: gridlay
excerpt: "VMG: People"
sitemap: false
permalink: /people/
---

<div style="width: 45%; height: auto; display: inline-block; vertical-align: top">         
   
   <img src="{{ site.url }}{{ site.baseurl }}/img/achutalarge.png" alt="Headshot" style="height:100%; width:100%">

</div>

<div markdown="1" style="width:45%; left: 50%; display: inline-block; margin: auto; padding-left: 50px">
   
   <br> <br>
   
   <h2>Achuta Kadambi</h2>
   
   <h4>Leader, Visual Machines Group</h4>
   
   Assistant Professor, UCLA
   Electrical and Computer Engineering
   PhD, Massachusetts Institute of Technology
    
 <a href="kadambi_cv.pdf">CV/Resume</a>
  
</div>




<div style="text-align:center">
   <br> <br> <br> 
   <h2> Postdoctoral Researchers <a href="{{ site.url }}{{ site.baseurl }}/vacancies">(Join Us)</a></h2>
   <br> <br> 
   <h2> Students</h2>
 </div>
 
 <br> <br>

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" alt="Insert photo" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.department }}<br>{{member.student}}<br> email: <{{ member.email }}></i>
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
