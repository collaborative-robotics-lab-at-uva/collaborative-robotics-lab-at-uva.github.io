---
title: "Collaborative Robotics Lab - Research"
layout: textlay
excerpt: "Collaborative Robotics Lab -- Research"
sitemap: false
permalink: /research/
---

# Research

{% assign number_printed = 0 %}
{% for research in site.data.researchs %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if research.highlight == 1  %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12">
 <div class="well">
  
  <pubtit>
  {%- if research.details_page -%}
  <a href="{{ site.url }}{{ site.baseurl }}/research_projects/{{ research.details_page}}">{{ research.title }}</a>
  {%- else -%}
  {{ research.title }}
  {%- endif -%}
  </pubtit>
  
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ research.image }}" class="img-responsive" width="33%" style="float: left; margin:15px" />
  <p>{{ research.description }}</p>
  <b> Team Members: {{ research.authors }}</b>
  <p><strong><a href="{{ research.link.url }}">{{ research.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ research.news1 }}</strong></p>
  <p> {{ research.news2 }} </p>
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