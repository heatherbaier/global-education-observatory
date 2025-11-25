---
layout: default
title: "Personnel Datasets"
---

<div class="max-w-4xl mx-auto py-10">
  <h1 class="text-3xl font-bold mb-6">Personnel Datasets</h1>

  <p class="text-gray-600 mb-6">
    Countries with personnel/teacher datasets:
  </p>

  <ul class="space-y-3">
    {% for item in site.personnel %}
      <li>
        <a href="{{ site.baseurl }}{{ item.url }}" 
           class="text-blue-600 hover:text-blue-800 text-lg">
          {{ item.country }}
        </a>
      </li>
    {% endfor %}
  </ul>
</div>
