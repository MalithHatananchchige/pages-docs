# API Reference

```markup
<!-- Initialize Pages core objects -->
<script type="text/javascript" src="pages/js/pages.min.js">
```

## **Environment variables**

Pages will detect the user OS and add it as a class name \(ex: 'windows', 'mac', 'unix', 'linux'\) into `body`.It will also detect if it's mobile device or desktop and add either 'mobile' and 'desktop' into the same tag.

## **Auto-initialized jQuery Plugins**

The following table shows which plugins are auto-initialized and their default configuration.

| PLUGIN | JQUERY |
| :--- | :--- |
| [Bootstrap Tooltip](http://getbootstrap.com/javascript/#tooltips) | Set `[data-toggle="tooltip"]` to any button or anchor tag. |
|  | `<a href="#" data-toggle="tooltip" data-placement="bottom" title="Print"><i class="fa fa-print"></i></a>` |
| [Select2](http://ivaynberg.github.io/select2/) | Set `[data-init-plugin="select2"]` |
| [Scrollbar](http://gromo.github.io/jquery.scrollbar/) | Set `class="scrollbar"`&lt;div style="height:200px" class="scrollbar"&gt;  ...&lt;/div&gt; |
| SelectFx | Set `[data-init-plugin="cs-select"]`&lt;select class="cs-select cs-skin-slide" data-init-plugin="cs-select"&gt;    &lt;option value="Websafe"&gt;Web-safe&lt;/option&gt;    &lt;option value="Helvetica"&gt;Helvetica&lt;/option&gt;    &lt;option value="SegeoUI"&gt;SegeoUI&lt;/option&gt;&lt;/select&gt; |
| [Unveil](http://luis-almeida.github.io/unveil/) | Applied to any `img` |

## **Utility functions**

$.Pages.isVisibleXs\(\)

Returns true if the current viewport is an extra small device. ex: Phones \(&lt;768px\)  


$.Pages.isVisibleSm\(\)

Returns true if the current viewport is a small device. ex: Tablets \(≥768px\)  


$.Pages.isVisibleMd\(\)

Returns true if the current viewport is a medium device. ex: Desktops \(≥992px\)  


$.Pages.isVisibleLg\(\)

Returns true if the current viewport is a large device. ex: Desktops \(≥1200px\)  


$.Pages.getUserAgent\(\)

Reads the pre-set user-agent class from `body` and returns either 'mobile' or 'desktop'  


$.Pages.setFullScreen\(element\)

Makes the given element to go full-screen mode. ex: `$.Pages.setFullScreen(document.querySelector('html'));`  


$.Pages.getColor\(color,opacity\)

Returns the `rgba` value for a given [Pages contextual color](http://pages.revox.io/dashboard/latest/html/condensed/color.html) and opacity.

## How to auto re-initialize Pages plugins

Pages JS has initialize third-party plugins like select2, selectfx etc using data attributes. Sometimes you want to reinitialize these plugins after AJAX or DOM change.  
  
Use the following link of code :

`$.Pages.init();`

