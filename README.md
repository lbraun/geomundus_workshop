# Open Source Geospatial Technologies: What, Why, and How
_A Workshop for GeoMundus 2018_

## Practical Exercise

_This excercise assumes you already have a github.com account. If not, create one here: [github.com](github.com)_

1. Create a new github pages repository following this guide:
[GitHub Pages](https://pages.github.com/)

2. Modify the index.html file in the respository you just created to look like this:
```html
<html>
  <head>
    <title>Nearst Weather Stations</title>
  </head>
  <body>
    <script>

    </script>
  </body>
</html>
```

3. Include Leaflet CSS file in the `<head>` section of your document:

```js
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.3.1/dist/leaflet.css" integrity="sha512-Rksm5RenBEKSKFjgI3a41vrjkw4EVPlJ3+OiI65vTjIdo9brlAacEuKOiQ5OFh7cOI1bkDwLqdLw3Zg0cRJAAQ==" crossorigin="" />
```

4. Include Leaflet JavaScript file right after Leaflet’s CSS:

```js
<script src="https://unpkg.com/leaflet@1.3.1/dist/leaflet.js" integrity="sha512-/Nsx9X4HebavoBvEBuyp3I7od5tA0UzAxs+j83KgC8PU0kgB4XiK4Lfe4y4cgBtaRJQEIFCW+oC506aPT2L1zw==" crossorigin=""></script>
```

5. Put a `<div>` element with a certain id inside the `<body>` section of your document:

```html
<div id="map" style="height:600px; width:100%">
</div>
```

6. Create your map in the `<script>` section of your document:

```js
var map = L.map("map").setView([38.732329, -9.160455], 10);

L.tileLayer('https://cartodb-basemaps-{s}.global.ssl.fastly.net/light_nolabels/{z}/{x}/{y}.png', {
  attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a> &copy; <a href="http://cartodb.com/attributions">CartoDB</a>',
  subdomains: 'abcd',
  maxZoom: 19
}).addTo(map);
```

Now you should have your basic map app running! Open the file in your browser to see.

## Adding to your map

### Markers

### Basic polygons

### APIs
