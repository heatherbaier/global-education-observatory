---
layout: default
title: "Global Education Observatory"
---

<div class="bg-gray-900 text-gray-100 py-10">
  <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-6 px-6">

    <!-- LEFT 1/3 -->
    <div>
      <h1 class="text-4xl font-extrabold leading-tight mb-4">
        Global Education Observatory
      </h1>
      <p class="text-gray-300 text-lg leading-relaxed">
        A global data portal for harmonized geospatial, school personnel,
        infrastructure, and educational outcomes data collected from multiple national sources.
      </p>
    </div>

    <!-- RIGHT 2/3 MAP -->
    <div class="md:col-span-2">
      <div id="map" class="h-72 rounded-xl shadow-lg"></div>
    </div>
  </div>
</div>

<!-- THEME CARDS ROW -->
<div class="bg-gray-100 py-8">
  <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-4 gap-6 px-6">

    <a href="/global-education-observatory/themes/geospatial.html"
       class="p-5 bg-white shadow rounded-xl hover:shadow-md transition">
        <h2 class="font-semibold text-xl text-gray-800">Geospatial</h2>
        <p class="text-gray-600 mt-1">Locations + boundaries</p>
    </a>

    <a href="/global-education-observatory/themes/personnel.html"
       class="p-5 bg-white shadow rounded-xl hover:shadow-md transition">
        <h2 class="font-semibold text-xl text-gray-800">Personnel</h2>
        <p class="text-gray-600 mt-1">Teachers & staffing</p>
    </a>
    
    <a href="/global-education-observatory/themes/resources.html"
       class="p-5 bg-white shadow rounded-xl hover:shadow-md transition">
        <h2 class="font-semibold text-xl text-gray-800">Resources</h2>
        <p class="text-gray-600 mt-1">Infrastructure & facilities</p>
    </a>
    
    <a href="/global-education-observatory/themes/outcomes.html"
       class="p-5 bg-white shadow rounded-xl hover:shadow-md transition">
        <h2 class="font-semibold text-xl text-gray-800">Outcomes</h2>
        <p class="text-gray-600 mt-1">Performance & enrollment</p>
    </a>

  </div>
</div>


<!-- Leaflet -->
<link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css"/>
<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
<script>
document.addEventListener("DOMContentLoaded", function() {
  var map = L.map('map').setView([10, 20], 2);

  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    maxZoom: 6,
    attribution: '© OpenStreetMap'
  }).addTo(map);
});
</script>
