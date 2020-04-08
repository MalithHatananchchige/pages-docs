# Google Maps

This section will guide you through how to setup a basic google map and add overlay colors to it,For more advance options please refer the google map developer API for Web [Google Map Developer API](https://developers.google.com/maps/documentation/javascript/tutorial)

## **Setting up a map**

**Step one**

Add the following google map api js, this is without private key. 

```markup
<script type="text/javascript" src="http://maps.google.com/maps/api/js?sensor=true"></script>
```

**Step Two**

Create an Empty div with an ID

```text
<div id="myMap"></div>
```

**Step Three**

Initialize Google Map.

```javascript
 // When the window has finished loading create our google map below
 google.maps.event.addDomListener(window, 'load', init);

var map;
var zoomLevel = 11;

 function init() {
     // Basic options for a simple Google Map
     // For more options see: https://developers.google.com/maps/documentation/javascript/reference#MapOptions
     var mapOptions = {
         // How zoomed in you want the map to start at (always required)
         zoom: zoomLevel,
         disableDefaultUI: true,
         // The latitude and longitude to center the map (always required)
         center: new google.maps.LatLng(40.6700, -73.9400), // New York
     };

     // Get the HTML DOM element that will contain your map 
     // We are using a div with id="map" seen below in the 
     var mapElement = document.getElementById('myMap');

     // Create the Google Map using out element and options defined above
     map = new google.maps.Map(mapElement, mapOptions);
 }
```

## **Map themes**

Google Maps comes with styling option that you can change, add the following `styles` attribute to `mapOptions` in the JS you created before

```javascript
styles: [{
   featureType: 'water',
   elementType: 'all',
   stylers: [{
       hue: '#e9ebed'
   }, {
       saturation: -78
   }, {
       lightness: 67
   }, {
       visibility: 'simplified'
   }]
}, {
   featureType: 'landscape',
   elementType: 'all',
   stylers: [{
       hue: '#ffffff'
   }, {
       saturation: -100
   }, {
       lightness: 100
   }, {
       visibility: 'simplified'
   }]
}, {
   featureType: 'road',
   elementType: 'geometry',
   stylers: [{
       hue: '#bbc0c4'
   }, {
       saturation: -93
   }, {
       lightness: 31
   }, {
       visibility: 'simplified'
   }]
}, {
   featureType: 'poi',
   elementType: 'all',
   stylers: [{
       hue: '#ffffff'
   }, {
       saturation: -100
   }, {
       lightness: 100
   }, {
       visibility: 'off'
   }]
}, {
   featureType: 'road.local',
   elementType: 'geometry',
   stylers: [{
       hue: '#e9ebed'
   }, {
       saturation: -90
   }, {
       lightness: -8
   }, {
       visibility: 'simplified'
   }]
}, {
   featureType: 'transit',
   elementType: 'all',
   stylers: [{
       hue: '#e9ebed'
   }, {
       saturation: 10
   }, {
       lightness: 69
   }, {
       visibility: 'on'
   }]
}, {
   featureType: 'administrative.locality',
   elementType: 'all',
   stylers: [{
       hue: '#2c2e33'
   }, {
       saturation: 7
   }, {
       lightness: 19
   }, {
       visibility: 'on'
   }]
}, {
   featureType: 'road',
   elementType: 'labels',
   stylers: [{
       hue: '#bbc0c4'
   }, {
       saturation: -93
   }, {
       lightness: 31
   }, {
       visibility: 'on'
   }]
}, {
   featureType: 'road.arterial',
   elementType: 'labels',
   stylers: [{
       hue: '#bbc0c4'
   }, {
       saturation: -93
   }, {
       lightness: -2
   }, {
       visibility: 'simplified'
   }]
}]
```



{% hint style="info" %}
For more google map Themes, try the following link [Google Map Themes](http://snazzymaps.com/)
{% endhint %}

