Leaflet.Spin
============

Shows a nice spin cursor on the map. See [online demo](http://makinacorpus.github.io/Leaflet.Spin/).

This plugin requires [Spin.js](http://fgnass.github.com/spin.js/).



Install
-----

### 0.1.1
Update bower dependencies
=======
### NPM

```
npm install leaflet-spin
```

### Bower

```
bower install leaflet-spin
```

### Manually

Download the [latest release](https://github.com/makinacorpus/Leaflet.Spin/releases/tag/1.0.0) and include it in your app


Usage
-----


### Manually

```javascript
map.spin(true);  // on
...
map.spin(false);  // off
```

### Spin.js options

You can control apparence of wheel by passing options on first ``spin()`` call.

```javascript
map.spin(true, {lines: 13, length: 40});
```

[More details on available options](http://fgnass.github.io/spin.js/)...


### With AJAX / JQuery

```javascript
map.spin(true);
$.ajax({url: 'http://server/api/'})
.done(function() {
  map.spin(false);
})
.error(function () {
  map.spin(false);
});
```


Using events:

```javascript
var layer = L.geoJson(null).addTo(map);

layer.fire('data:loading');
$.getJSON('http://server/path.geojson', function (data) {
    layer.fire('data:loaded');
    layer.addData(data);
});
```

### With [Leaflet.AJAX](https://github.com/calvinmetcalf/leaflet-ajax/)

```javascript
var layer = L.geoJson.ajax();
layer.addUrl('http://server/path.geojson');
```

Changelog
-----

### 1.0.0
This version is stable

### 0.1.1
Update bower dependencies

### 0.1.0
Initial version



Authors
-------

[![Makina Corpus](http://depot.makina-corpus.org/public/logo.gif)](http://makinacorpus.com)
