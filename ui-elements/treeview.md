# Treeview

Tree view in Pages are powered by [jQuery Dynatree ](https://github.com/mar10/dynatree), which is a Drag & drop hierarchical list with mouse and touch compatibility Follow these steps to initialize nest-tables in your page

**Step one**

Include the following stylesheet inside the `<head>`

```markup
<link href="assets/plugins/jquery-dynatree/skin/ui.dynatree.css" rel="stylesheet" type="text/css" media="screen"/>
```

**Step two**

Include the relevant javascript files inside the `<body>` before core template script inclusions

```markup
<script src="assets/plugins/jquery-dynatree/jquery.dynatree.min.js" type="text/javascript">
```

**Step three**

1. Create a DIV and give it a unique ID, we are going to use this to initialize the plugin
2. Inside this DIV, create a list of unordered items using UL LI
3. Make sure you have unique ID for each of UL and LI tags

```markup
<div class="m-b-20" id="default-tree">
  <ul id="treeData" style="display: none;">
    <li id="id1" title="Look, a tool tip!">item1 with key and tooltip
    </li>
    <li id="id2">item2
    </li>
    <li class="folder" id="id3">Folder with some children
      <ul>
        <li id="id3.1">Sub-item 3.1
          <ul>
            <li id="id3.1.1">Sub-item 3.1.1
            </li>
            <li id="id3.1.2">Sub-item 3.1.2
            </li>
          </ul>
        </li>
        <li id="id3.2">Sub-item 3.2
          <ul>
            <li id="id3.2.1">Sub-item 3.2.1
            </li>
            <li id="id3.2.2">Sub-item 3.2.2
            </li>
          </ul>
        </li>
      </ul>
    </li>
    <li class="expanded" id="id4">Document with some children (expanded on
    init)
      <ul>
        <li class="active focused" id="id4.1">Sub-item 4.1 (active and focus on
        init)
          <ul>
            <li id="id4.1.1">Sub-item 4.1.1
            </li>
            <li id="id4.1.2">Sub-item 4.1.2
            </li>
          </ul>
        </li>
        <li id="id4.2">Sub-item 4.2
          <ul>
            <li id="id4.2.1">Sub-item 4.2.1
            </li>
            <li id="id4.2.2">Sub-item 4.2.2
            </li>
          </ul>
        </li>
      </ul>
    </li>
  </ul>
</div>
```

**Step Four**

Initialize the plugin

```markup
<script>
$(document).ready(function() {
      $("#default-tree").dynatree({
       fx: { height: "toggle", duration: 200 }//Slide down animation
    });
});
</script>
```

