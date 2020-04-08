# Charts

Pages comes bundled with two popular charting libraries: [Rickshaw](http://code.shutterstock.com/rickshaw/) and [NVD3](http://pages.revox.io/dashboard/3.0.0/docs/partials/nvd3.org). These libraries render charts in SVG format which makes them highly customizable using CSS and JS.

## **Rickshaw Charts**

Rickshaw is a simple framework for drawing charts of time series data on a web page, built on top of Mike Bostock's delightful D3 library. These charts can be powered by static historical data sets, or living data that continuously updates in real time.  


Please refer to [Rickshaw Tutorial](http://code.shutterstock.com/rickshaw/tutorial/introduction.html) to learn more about the library

**Step one**

Include the plugin stylesheet rickshaw.min.css.css `<head>`

```markup
<link type="text/css" rel="stylesheet" href="assets/plugins/rickshaw/rickshaw.min.css"></link>
```

**Step two**

Include the plugin javascript file and D3 library inside the `<body>`before core template script inclusions, if it's not there already. 

```markup
<script src="assets/plugins/d3/d3.min.js"></script>
<script src="assets/plugins/rickshaw/rickshaw.min.js"></script>
```

**Step three**

Create the markup

```markup
<div id="chart"></div>
```

**Step four**

Apply the plugin. This example renders a basic area chart

```markup
<script>

var data = [ { x: 0, y: 40 }, { x: 1, y: 49 }, { x: 2, y: 17 }, { x: 3, y: 42 } ];

var graph = new Rickshaw.Graph( {
        element: document.querySelector("#chart"),
        width: 580,
        height: 250,
        series: [ {
                color: 'steelblue',
                data: data
        } ]
} );

graph.render();

</script>
```

**Step three**

Add following markup to your page. Note the use of directive `rickshaw`

```markup
<rickshaw
    rickshaw-options="options"
    rickshaw-features="features"
    rickshaw-series="series">
</rickshaw>
```

## **NVD3 Charts**

NVD3 is an attempt to build re-usable charts and chart components for d3.js without taking away the power that d3.js gives you.

{% hint style="info" %}
Please refer to [NVD3 Tutorial](http://nvd3.org/examples/index.html) to learn about the basics of the library
{% endhint %}

**Step one**

Include the plugin stylesheet rickshaw.min.css.css `<head>`.

```text
<link media="screen" type="text/css" rel="stylesheet" href="assets/plugins/nvd3/nv.d3.min.css"></link>
```

**Step two**

Include the plugin javascript files inside the `<body>`before core template script inclusions, if it's not there already. 

```markup
<script type="text/javascript" src="assets/plugins/nvd3/lib/d3.v3.js"></script>
<script type="text/javascript" src="assets/plugins/nvd3/nv.d3.min.js"></script>
<script type="text/javascript" src="assets/plugins/nvd3/src/utils.js"></script>
<script type="text/javascript" src="assets/plugins/nvd3/src/tooltip.js"></script>
<script type="text/javascript" src="assets/plugins/nvd3/src/interactiveLayer.js"></script>
<script type="text/javascript" src="assets/plugins/nvd3/src/models/axis.js"></script>
<script type="text/javascript" src="assets/plugins/nvd3/src/models/line.js"></script>
<script type="text/javascript" src="assets/plugins/nvd3/src/models/lineWithFocusChart.js"></script>
```

**Step three**

Create the markup. Apply the class `line-chart` to get the Pages pre-defined style for NVD3 charts. Use data-attributes to customize the style

```markup
<div id="nvd3" class="line-chart" 
  data-line-color="success" 
  data-area-color="master"
  data-points="true" 
  data-point-color="white" 
  data-stroke-width="2">
    <svg></svg>
</div>
```

Available data attributes:

| `DATA ATTRIBUTE` | `AVAILABLE VALUES` | `DESCRIPTION` |
| :--- | :--- | :--- |
| `data-line-color` | white \| master \| success \| info \| complete \| primary \| warning \| danger | Change the line color of a line chart |
| `data-area-color` | white \| master \| success \| info \| complete \| primary \| warning \| danger | Change the area color of a line chart with area option |
| `data-points` | true \| false | Show/hide point circles |
| `data-point-color` | white \| master \| success \| info \| complete \| primary \| warning \| danger | Change the point color |
| `data-stroke-width` | 1 \| 2 \| 3 | Change the stroke width of a line chart. Values are in pixels |

## **Sparkline Charts**

This jQuery plugin generates sparklines \(small inline charts\) directly in the browser using data supplied either inline in the HTML, or via javascript.  


{% hint style="info" %}
Please refer to [Sparkline Documentation](http://omnipotent.net/jquery.sparkline/#s-about) to learn more about the library
{% endhint %}

**Step one**

Include the plugin javascript files inside the `<body>`before core template script inclusions, if it's not there already. Please view [jQuery plugin inclusion guideline rules](http://pages.revox.io/dashboard/3.0.0/docs/partials/js_rules.html)

```markup
<script type="text/javascript" src="assets/plugins/jquery-sparkline/jquery.sparkline.min.js"></script>
```

**Step two**

Create the markup.

```markup
<div id="sparkline"></div>
```

**Step three**

Apply the plugin. This example renders a basic line chart

```markup
<script>

$("#sparkline").sparkline([5,6,7,9,9,5,3,2,2,4,6,7], {type: 'line'});

</script>
```

