---
layout: default
title: "Resources & Infrastructure Datasets"
---

<div class="max-w-5xl mx-auto py-10">

  <h1 class="text-4xl font-bold mb-6 text-gray-800">Resources & Infrastructure Datasets</h1>

  <p class="text-gray-600 mb-8 text-lg">
    Resources & Infrastructure data.
  </p>

  <!-- Grid of cards -->
  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">

    {% for item in site.resources %}
      <a href="{{ site.baseurl }}{{ item.url }}"
         class="block bg-white border border-gray-200 rounded-xl shadow-sm hover:shadow-md hover:border-blue-400 transition p-6">

          <!-- Icon -->
          <div class="flex items-center mb-4">
            <span class="material-icons text-blue-600 text-3xl mr-3">public</span>
            <h2 class="text-xl font-semibold text-gray-800">{{ item.country }}</h2>
          </div>

          <p class="text-gray-600 text-sm">
            Click to view dataset
          </p>

      </a>
    {% endfor %}

  </div>
</div>

<!-- Google Material Icons -->
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
