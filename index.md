<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Global Education Data Portal</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <!-- Tailwind -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Leaflet -->
  <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
  <script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>

</head>
<body class="bg-gray-50 text-gray-800">

  <!-- HEADER -->
  <header class="bg-white shadow p-6 mb-6">
    <h1 class="text-3xl font-bold text-center">Global Education Data Portal</h1>
    <p class="text-center text-gray-500 text-lg mt-1">
      Explore geospatial, personnel, infrastructure, and outcomes data.
    </p>
  </header>

  <!-- MAP -->
  <div class="max-w-5xl mx-auto mb-10">
    <div id="map" class="h-96 rounded-xl shadow"></div>
  </div>

  <script>
    var map = L.map('map').setView([10, 20], 2); // default world view

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      maxZoom: 6,
      attribution: '© OpenStreetMap'
    }).addTo(map);
  </script>

  <!-- THEME CARDS -->
  <div class="max-w-5xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-6 pb-20">

    <a href="themes/geospatial.html"
       class="p-6 bg-white rounded-xl shadow hover:shadow-lg transition">
      <h2 class="text-xl font-semibold">Geospatial</h2>
      <p class="text-gray-600 mt-2">Boundary files, school locations, admin layers.</p>
    </a>

    <a href="themes/personnel.html"
       class="p-6 bg-white rounded-xl shadow hover:shadow-lg transition">
      <h2 class="text-xl font-semibold">Personnel</h2>
      <p class="text-gray-600 mt-2">Teacher counts, PTRs, qualifications.</p>
    </a>

    <a href="themes/resources.html"
       class="p-6 bg-white rounded-xl shadow hover:shadow-lg transition">
      <h2 class="text-xl font-semibold">Resources & Infrastructure</h2>
      <p class="text-gray-600 mt-2">Classrooms, electricity, WASH, materials.</p>
    </a>

    <a href="themes/outcomes.html"
       class="p-6 bg-white rounded-xl shadow hover:shadow-lg transition">
      <h2 class="text-xl font-semibold">Outcomes</h2>
      <p class="text-gray-600 mt-2">NAT scores, dropout, completion rates.</p>
    </a>

  </div>

</body>
</html>
