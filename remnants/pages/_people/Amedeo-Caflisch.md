---
title: "Amedeo Caflisch"
layout: default
date: 1996-07-01
excerpt_separator: <!--more-->
excerpt_link: 'http://www.biochem-caflisch.uzh.ch'
image_file: 'Caflisch.png'
category:
  - people
tags:
  - UZH
  - previous_teachers
---

{% for static_file in site.static_files %}
  {% if static_file.path contains page.image_file %}
<img style="float: right; max-width: 60px;" src="{{ static_file.path | relative_url}}" />
  {% endif %}
{% endfor %}

## {{ page.title }}

* Professor of Computational Structural Biology
* Department of Biochemistry
* University of Zürich

<!--more-->
