# Datepicker

Datepicker controls in Pages are powered by [Bootstrap Datepicker](https://github.com/eternicode/bootstrap-datepicker) plugin.

{% hint style="info" %}
Please refer to [Bootstrap Datepicker Documentation](https://bootstrap-datepicker.readthedocs.io/en/stable/) to learn about plugin options
{% endhint %}

**Step one**

Include the stylesheet `datepicker3.css` inside the `<head>` if it's not there already.

```markup
<link media="screen" type="text/css" rel="stylesheet" href="assets/plugins/bootstrap-datepicker/css/datepicker3.css">
```

**Step two**

Include the relevant javascript files inside the `<body>` before core template script inclusions, if it's not there already.

```markup
<script type="text/javascript" src="assets/plugins/bootstrap-datepicker/js/bootstrap-datepicker.js">
```

**Step three**

Add the markup

```markup
<div id="myDatepicker" class="input-group date">
    <input type="text" class="form-control">
    <span class="input-group-addon"><i class="fa fa-calendar"></i>
    </span>
</div>
```

**Step four**

Apply the plugin.

{% hint style="warning" %}
Make sure you place the following script **below** all the pre-requisites mentioned in the Step two above.
{% endhint %}

![](../.gitbook/assets/datepicker.png)

```markup
<script>
$(document).ready(function() {
    $('#myDatepicker').datepicker();
});
</script>
```

