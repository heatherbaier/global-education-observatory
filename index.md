---
layout: default
title: Global Education Observatory
---

<!-- HERO SECTION WITH FULL-WIDTH MAP -->
<div class="relative w-full h-[400px] md:h-[500px]">
  <div id="map" class="absolute inset-0"></div>
  <div class="absolute inset-0 bg-black/40 flex items-center justify-center">
    <h1 class="text-white text-4xl md:text-6xl font-bold tracking-wide drop-shadow-lg">
      Global Education Observatory
    </h1>
  </div>
</div>

<!-- THEME GRID -->
<div class="max-w-6xl mx-auto py-12 px-6">

  <h2 class="text-2xl text-white font-semibold mb-8">
    Explore Education Data by Theme
  </h2>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-6">

    <!-- Geospatial -->
    <a href="/global-education-observatory/themes/geospatial.html"
       class="bg-gray-900 border border-gray-700 hover:border-blue-500 transition p-6 rounded-xl flex items-center space-x-4">
      <img src="https://cdn-icons-png.flaticon.com/512/684/684908.png"
           class="h-12 opacity-80">
      <span class="text-xl text-gray-200">Geospatial</span>
    </a>

    <!-- Personnel -->
    <a href="/global-education-observatory/themes/personnel.html"
       class="bg-gray-900 border border-gray-700 hover:border-blue-500 transition p-6 rounded-xl flex items-center space-x-4">
      <img src="https://cdn-icons-png.flaticon.com/512/1995/1995573.png"
           class="h-12 opacity-80">
      <span class="text-xl text-gray-200">Personnel</span>
    </a>

    <!-- Resources -->
    <a href="/global-education-observatory/themes/resources.html"
       class="bg-gray-900 border border-gray-700 hover:border-blue-500 transition p-6 rounded-xl flex items-center space-x-4">
      <img src="https://cdn-icons-png.flaticon.com/512/3062/3062634.png"
           class="h-12 opacity-80">
      <span class="text-xl text-gray-200">Resources & Infrastructure</span>
    </a>

    <!-- Outcomes -->
    <a href="/global-education-observatory/themes/outcomes.html"
       class="bg-gray-900 border border-gray-700 hover:border-blue-500 transition p-6 rounded-xl flex items-center space-x-4">
      <img src="https://cdn-icons-png.flaticon.com/512/2548/2548585.png"
           class="h-12 opacity-80">
      <span class="text-xl text-gray-200">Learning Outcomes</span>
    </a>

  </div>
</div>

<script>
var map = L.map('map', {
  zoomControl: false,
  scrollWheelZoom: false,
  dragging: false
}).setView([20, 10], 2);

L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
  attribution: ''
}).addTo(map);
</script>
