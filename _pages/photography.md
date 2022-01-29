---
title: "Photography"
permalink: /photography/
layout: collection
# collection: posts
entries_layout: grid
author_profile: true
---

{% assign image_files = site.static_files | where: "photography_image", true | sort: "basename" | reverse %}

<figure class="third">
{% for image in image_files %}
{% assign path = image.path %}
<a class="image-popup" href="{{ path }}">
  <img src="{{ path }}" class ="lazyload" />
</a>
{% endfor %}
</figure>