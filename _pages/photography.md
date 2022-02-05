---
title: "Photography"
permalink: /photography/
# layout: collection
# collection: posts
# entries_layout: grid
author_profile: true
---

{% assign image_files = site.static_files | where: "photography_image", true | sort: "basename" | reverse %}

<div class="photography-gallery">
<!-- <figure class="third"> -->
{% assign image_count = 0 %}

{% for image in image_files %}
  {% assign image_count = image_count | plus: 1 %}
  {% assign path = image.path %}
  <!-- {% assign mod = image_count | modulo: 7 %} -->

  <!-- {% if mod == 1 %}
    <div class ="photography-gallery-column">
  {% endif %} -->
  <!-- <div class="photography-gallery-container"> -->
  <a class="image-popup" href="{{ path }}">
    <img data-src="{{ path }}" class ="lazyload" />
  </a>
  <!-- </div> -->

  <!-- {% if mod == 0 or forloop.last %}
    </div>
  {% endif %} -->
{% endfor %}
</div>
<!-- </figure> -->