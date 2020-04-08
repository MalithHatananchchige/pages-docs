# Summernote

{% hint style="info" %}
Please refer to [Summernote Documentation](http://hackerwins.github.io/summernote) to learn about plugin options
{% endhint %}

**Step one**

Include the stylesheet `summernote.css` inside the `<head>`

```markup
<link media="screen" type="text/css" rel="stylesheet" href="assets/plugins/summernote/css/summernote.css">
```

**Step two**

Include the javascript file inside the `<body>`before core template script inclusions.

```markup
<script type="text/javascript" src="assets/plugins/summernote/js/summernote.min.js"></script>
```

**Step three**

Add the markup.

```markup
<div id="summernote">Hello Summernote</div>
```

**Step four**

Apply the plugin.

{% hint style="warning" %}
Make sure you place the following script **below** all the pre-requisites mentioned in the Step two above.
{% endhint %}

![](../.gitbook/assets/screen-shot-2018-06-04-at-7.04.55-pm%20%281%29.png)

```markup
<script>
$(document).ready(function() {
   $('#summernote').summernote();
});
</script>
```

