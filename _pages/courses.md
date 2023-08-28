---
title: "Courses"
layout: gridlay
excerpt: "Courses"
sitemap: false
permalink: /courses 
---


<p align="center">
  Courses
</p>


At qxresearch AI, we are passionate about fostering the next generation of computer scientists and researchers. We firmly believe that empowering young minds with knowledge and skills in artificial intelligence and machine learning will shape a brighter future for technology and society as a whole. As part of our commitment to education and knowledge-sharing, we are thrilled to introduce our personalized 1-to-1 `Python`, `Data Structures` and `Machine Learning` Sessions designed specifically for students. 

The course is designed with a dual purpose: not only to foster academic research, but also to elevate students' problem-solving acumen through immersive engagement with `LeetCode` challenges. Furthermore, the course culminates with students embarking on a significant Python-based project, thereby playing a pivotal role in realizing this comprehensive objective.

<br>


<p style="text-align: center;">Find the archive of research projects and papers developed by our team and our students : [here](https://github.com/qxresearch/qxresearch-event-1)</p>


<br>

{% assign number_printed = 0 %}
{% for publi in site.data.courses %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.duration }}</em></p>
  <p><em>{{ publi.fees }}</em></p>
  <p><em>{{ publi.modules }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>

<br>
