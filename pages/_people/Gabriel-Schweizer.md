---
title: "Gabriel Schweizer"
layout: default
date: 2020-11-10
excerpt_separator: <!--more-->
excerpt_link: 'https://www.ieu.uzh.ch/en/staff/member/schweizer_gabriel.html'
image_file: 'Schweizer.jpg'
category:
  - people
tags:
  - UZH
  - teachers
  - BIO390
---

{% for static_file in site.static_files %}
  {% if static_file.path contains page.image_file %}
<img style="float: right; max-width: 60px;" src="{{ static_file.path | relative_url}}" />
  {% endif %}
{% endfor %}

## {{ page.title }}

* Postdoctoral Researcher
* Department of Evolutionary Biology and Environmental Studies
* University of Zurich

<!--more-->
