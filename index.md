---
layout: default
title: "Global Education Observatory"
---

<!-- Hero Section -->
<div class="max-w-5xl mx-auto text-center py-10">
  <h1 class="text-4xl font-bold text-gray-800">Global Education Observatory</h1>
  <p class="text-lg text-gray-600 mt-4">
    Explore harmonized education datasets across geospatial, personnel, resources, and learning outcomes domains.
  </p>
</div>

<!-- Leaflet Map -->
<div class="max-w-5xl mx-auto mb-10">
  <div id="map" class="h-96 w-full rounded-xl shadow"></div>
</div>

<!-- Theme Cards -->
<div class="max-w-5xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-6 pb-20">

  <a href="/global-education-observatory/themes/geospatial.html" 
     class="p-6 bg-white rounded-xl shadow hover:shadow-lg transition">
    <h2 class="text-xl font-semibold">Geospatial</h2>
    <p class="text-gray-600 mt-2">Boundary files, school locations, administrative layers.</p>
  </a>

  <a href="/global-education-observatory/themes/personnel.html" 
     class="p-6 bg-white rounded-xl shadow hover:shadow-lg transition">
    <h2 class="text-xl font-semibold">Personnel</h2>
    <p class="text-gray-600 mt-2">Teacher counts, qualifications, pupil-teacher ratios.</p>
  </a>

  <a href="/global-education-observatory/themes/resources/" 
     class="p-6 bg-white rounded-xl shadow hover:shadow-lg transition">
    <h2 class="text-xl font-semibold">Resources & Infrastructure</h2>
    <p class="text-gray-600 mt-2">Electricity, classrooms, water, sanitation, infrastructure.</p>
  </a>

  <a href="/global-education-observatory/themes/outcomes/" 
     class="p-6 bg-white rounded-xl shadow hover:shadow-lg transition">
    <h2 class="text-xl font-semibold">Learning Outcomes</h2>
    <p class="text-gray-600 mt-2">Test scores, dropout, completion rates, transitions.</p>
  </a>

  {{ site.geospatial | size }} geospatial datasets<br>
  {{ site.personnel | size }} personnel datasets<br>
  {{ site.baseurl }}
    

</div>

<!-- Load Leaflet -->
<link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css"/>
<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>

<!-- Load Tailwind Safely -->
<script src="https://cdn.tailwindcss.com"></script>

<script>
document.addEventListener("DOMContentLoaded", function() {

  // Initialize the map
  var map = L.map('map').setView([10, 20], 2);



  L.tileLayer('https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png', {
    maxZoom: 6,
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors &copy; <a href="https://carto.com/attributions">CARTO</a>'
  }).addTo(map);

  const countryList = [
      {% for file in site.static_files %}
        {% if file.path contains '/data/geospatial/' %}
          "{{ file.basename | slice: 0, 3 }}",
        {% endif %}
      {% endfor %}
    ];

  // Loop each WMS layer
  countryList.forEach(iso => {
    L.tileLayer.wms("https://globaleducationobservatory.org/geoserver/geo/wms", {
      layers: `geo:${iso}_adm0`,
      format: 'image/png',
      transparent: true,
      version: '1.1.0',
      attribution: "Global Education Observatory"
    }).addTo(map);
  });

});
</script>
