---
layout: default
title: "Geospatial Datasets"
---

<div class="max-w-4xl mx-auto py-10">
  <h1 class="text-3xl font-bold mb-6">Geospatial Datasets</h1>

  <p class="text-gray-600 mb-6">
    Countries with geospatial datasets available:
  </p>

  <ul>
  {% for staff_member in site.geospatial %}
  <h2>
    <a href="{{ staff_member.url }}">
      {{ staff_member.country }}
    </a>
  </h2>
    {% endfor %}
  </ul>




  <!-- <ul class="space-y-3">
    {% for country in site.geospatial %}
      <li>
        <a href="{{ item.url }}" class="text-blue-600 hover:text-blue-800 text-lg">
          {{ country.country }}
        </a>
      </li>
    {% endfor %}
  </ul> -->

    


</div>
