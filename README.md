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

You can add [basic markers](https://leafletjs.com/reference-1.3.4.html#marker) to your map by adding the following code in the `<script>` section of your document:

```js
L.marker([38.732235, -9.160366]).addTo(map);
```

### Polygons

You can add [basic polygons](https://leafletjs.com/reference-1.3.4.html#polygon) to your map by adding the following code in the `<script>` section of your document:

```js
// Create a red polygon from an array of lat-long points
var points = [
  [38.73098724394945, -9.159668684005737],
  [38.73015866055299, -9.159711599349976],
  [38.73011681265176, -9.158810377120972],
  [38.7306022467989, -9.157898426055908],
  [38.731414086190945, -9.157887697219849],
  [38.73149778044903, -9.158896207809448],
  [38.73098724394945, -9.159668684005737]
];
var polygon = L.polygon(points, {color: 'red'}).addTo(map);
```



### APIs
