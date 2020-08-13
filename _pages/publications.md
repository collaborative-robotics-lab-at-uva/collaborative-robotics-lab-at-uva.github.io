---
title: "Collaborative Robotics Lab - Publications"
layout: gridlay
excerpt: "Collaborative Robotics Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

{% assign tm_pub_year = 0 %}

<div class="container">
{% for publi in site.data.publist %}

  {%- if publi.pub_year != tm_pub_year -%}
  <h4>{{ publi.pub_year }} </h4>
    {%- assign tm_pub_year = publi.pub_year -%}
  {%- endif -%}

  <div class="col-sm-12">
  <b>{{ publi.title }}</b> <br />
  {{ publi.authors }} <br/>
  <em>{{publi.pub_venue}}, {{publi.pub_date}}</em> <br/>
  <div class="container">

  <div class="row">
  {%- if publi.link.bibtex_filename -%}
  <a href="{{ site.url }}{{ site.baseurl }}/files/bibtex/{{ publi.link.bibtex_filename }}" class="btn btn-warning btn-rounded btn-xs" role="button" target="_blank">BibTex</a>
  {% endif %}

  {%- if publi.link.pdf_filename -%}
  <a href="{{ site.url }}{{ site.baseurl }}/files/papers/{{ publi.link.pdf_filename }}" class="btn btn-warning btn-xs btn-rounded" role="button" target="_blank">PDF</a>
  {% endif -%}
  
  {%- if publi.link.url -%}
  <a href="{{ publi.link.url }}" class="btn btn-warning btn-xs btn-rounded" role="button" target="_blank">{{publi.link.display}}</a>
  {% endif -%}
  
  </div></div>
  </div>
{%- endfor -%}

</div>
