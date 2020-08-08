---
title: "Collaborative Robotics Lab - Publications"
layout: gridlay
excerpt: "Collaborative Robotics Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em> <a href="{{ publi.link.url }}">{{ publi.link.display }}</a> <br />
  <a href="{{ site.url }}{{ site.baseurl }}/bibtex/{{ publi.link.bibtex_filename }}" class="btn btn-primary" role="button" target="_blank">BibTex</a>
  <a href="{{ publi.link.pdf_url }}" class="btn btn-primary" role="button" target="_blank">PDF</a>

{% endfor %}
