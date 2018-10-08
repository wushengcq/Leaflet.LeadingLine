# Leaflet Animated Sector

This is a Leaflet plugin for drawing the leading line with arrow pattern in it. Feedback appreciated !

## Online demo

<https://wushengcq.github.io/demo/leading-line/index.html>

![example screenshot](/example/example.png)

## How can I use it?

1. Import the plugin js file in your page. 

2. The following code will create an leading-line on map, assuming a `Leaflet.Map` called `map`.

```javascript
var route = [
	[29.558176, 106.510338], 
	[28.200825, 112.98127],
	[30.567514, 114.291939], 
	[31.863255, 117.275703], 
	[31.106981, 121.37156] 
];

// create a leading-line
var leadingLine = L.leadingLine(route, {
	color: '#00ff00',       // color of line
	weight: 20,             // the line width 
	borderSize: 2,          
	borderColor: '#888888', 
	signColor: '#048A3E',   // color of arrow pattern
	signInterval: 60,       // interval between two arrow
	opacity: 1, 
}).addTo(_map);

map.fitBounds(leadingLine.getBounds());
```

