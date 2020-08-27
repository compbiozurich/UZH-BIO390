---
title: 'BIO390 HS20 Programme'
layout: default
author:
  - "@mbaudis"
excerpt_separator: <!--more-->
www_link: 						# web address, e.g. https://www.ga4gh.org; auto-linked
pdf_file_name: 				# name of PDF (no path) somewhere in "assets"; auto-linked
www_links_formatted:  # one or more formatted html links
  - '<a href="/UZH-BIO390/">[UZH-BIO390]</a>'
  - '<a href="/UZH-BIO390/categories/people.html">[Course Lecturers]</a>'
categories:
  - news
tags:
  - days
  - "2020"
---

## {{ page.title }}

Two weeks before the start of the lectures we present the (non-final) program for
the 2020 Autumn lectures in the "Introduction to Bioinformatics"  series at the
University of Zurich.

<!--more-->

#### Lecturers & Topics

Please also see the [individual pages]({{"/UZH-BIO390/categories/lectures.html" | relative_link}}) lecture pages for more information.

#### Individual Lectures

{%- assign today = site.time | date: '%Y%m%d' -%}
{%- assign current_year = site.time | date: '%Y' -%}
{%- assign this_category = "lectures" -%}

{%- assign cat_posts = site.emptyArray -%}
{%- for post in site.documents -%}
  {%- if post.categories contains this_category -%}
    {%- assign post_year = post.date | date: '%Y' -%}
    {%- unless current_year != post_year -%}
      {% unless post.tags contains '.prepend' or post.tags contains '.append' %}
        {%- assign cat_posts = cat_posts | push: post -%}
      {% endunless %}
    {% endunless %}
  {%- endif -%}
{%- endfor -%}
{%- assign cat_posts = cat_posts | sort: 'date' -%}

{%- for post in cat_posts -%}
  {%- assign post_author = post.author | downcase -%}
  {%- assign excerpt_link = post.url | relative_url -%}
  {%- assign post_day = post.date | date: "%Y-%m-%d" -%}
<div class="excerpt">
<h4>{{ post_day }}</h4>
<a href="{{ excerpt_link }}">{{ post.excerpt }}</a>
<p class="footnote">
  {%- if post.author -%}{{ post.author | join: " | " }}&nbsp;{%- endif -%}
  {%- if post.date -%}{{ post.date | date: "%Y-%m-%d" }}: {% endif %}
<a href="{{ excerpt_link }}">more ...</a>
</p>
</div>
{%- endfor -%}
