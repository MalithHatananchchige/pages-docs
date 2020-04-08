# Typehead

These are also know as auto-fill input boxes that fills up while you type. This is powered by Bootstrap type-head.

{% hint style="info" %}
You can view there official documentation [here](https://twitter.github.io/typeahead.js/examples/)
{% endhint %}

**Step One**

Include the required javascript files inside the `<body>` before core template script inclusions, if they are not there already.

```markup
<script src="assets/plugins/bootstrap-typehead/typeahead.bundle.min.js"></script>
<script src="assets/plugins/bootstrap-typehead/typeahead.jquery.min.js"></script>
```

**Step Two**

Create a simple text box field and give it an ID so you can initialize in your JS file

```markup
<div class="form-group">
<input class="typeahead form-control" id="mytyphead" type="text" placeholder="States of USA">
</div>

<form class="" role="form">
<div class="form-group form-group-default required typehead" id="sample-three">
<label>Countries</label>
<input class="typeahead form-control" id="mytyphead" type="text" placeholder="States of USA">
</div>
</form>
```

**Step Three**

Initialize your typehead with the ID you use

```javascript
        var countries = new Bloodhound({
          datumTokenizer: Bloodhound.tokenizers.whitespace,
          queryTokenizer: Bloodhound.tokenizers.whitespace,
          prefetch: 'http://pages.revox.io/json/countries-list.json'
        });

        // passing in `null` for the `options` arguments will result in the default
        // options being used
        $('#mytyphead').typeahead(null, {
          name: 'countries',
          source: countries
        });
```

