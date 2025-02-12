# my-gis-map
**<!DOCTYPE html>
<html>
<head>
    <title>My GIS Map</title>
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />
    <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>
</head>
<body>
    <div id="map" style="height: 500px;"></div>
    <script>
        var map = L.map('map').setView([20.5937, 78.9629], 5); // India Map

        L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            attribution: '&copy; OpenStreetMap contributors'
        }).addTo(map);

        // Load GeoJSON data
        fetch('data.geojson')
            .then(response => response.json())
            .then(data => {
                L.geoJSON(data).addTo(map);
            });
    </script>
</body>
</html>**

