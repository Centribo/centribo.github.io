---
title: "Photography"
permalink: /photography/
layout: collection
# collection: posts
entries_layout: grid
author_profile: true
---

{% assign image_files = site.static_files | where: "photography_image", true | sort: "modified_time" %}
<!-- {{ image_files | sort: "modified_time" }} -->

<figure class="third">
{% for myimage in image_files %}
<a class="image-popup" href="{{ myimage.path }}">
  <img src="{{ myimage.path }}"/>
</a>
{% endfor %}
</figure>