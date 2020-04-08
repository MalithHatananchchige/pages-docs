# Nestable

Nestables in Pages are powered by [jQuery Nestables](https://github.com/dbushell/Nestable) which is a Drag & drop hierarchical list with mouse and touch compatibility Follow these steps to initialize nestables in your page

**Step one**

Include the stylesheet `jquery.nestable.css` inside the `<head>`

```markup
<link media="screen" type="text/css" rel="stylesheet" href="assets/plugins/jquery-nestable/jquery.nestable.css">
```

**Step two**

Include the relevant javascript files inside the `<body>` before core template script inclusions

```markup
<script type="text/javascript" src="assets/plugins/jquery-nestable/jquery.nestable.js"></script>
```

**Step three**

Apply the plugin to your desired element

```markup
<!-- Element to be used with the plugin -->
<div class="dd" id="basic_example">
    <ol class="dd-list">
        <li class="dd-item" data-id="1">
            <div class="dd-handle">
                Item 1
            </div>
        </li>
        <li class="dd-item" data-id="2">
            <div class="dd-handle">
                Item 2
            </div>
            <ol class="dd-list">
                <li class="dd-item" data-id="3">
                    <div class="dd-handle">
                        Item 3
                    </div>
                </li>
                <li class="dd-item" data-id="4">
                    <div class="dd-handle">
                        Item 4
                    </div>
                </li>
                <li class="dd-item" data-id="5">
                    <div class="dd-handle">
                        Item 5
                    </div>
                </li>
            </ol>
        </li>
    </ol>
</div>

<script>
$(document).ready(function() {
    // Apply the plugin to the element
     $('#basic_example').nestable();
});
</script>
```

