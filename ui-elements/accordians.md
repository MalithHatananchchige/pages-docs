# Collapse

Collapse are created using [Bootstrap Native ](https://getbootstrap.com/docs/4.1/components/collapse/)Collapse, they will work as the same way how it works in bootstrap, but it is styled to pages color scheme.To add a modal to pages please refer following guidelines

[Bootstrap Collapse Guideline ](https://getbootstrap.com/docs/4.1/components/collapse/)

Place this HTML code in any Pages html file

```markup
<div class="panel panel-group panel-transparent" data-toggle="collapse" id=
"accordion">
  <div class="panel panel-default">
    <div class="panel-heading">
      <h4 class="panel-title">
        <a class="collapsed" data-parent="#accordion" data-toggle=
        "collapse" href="#collapseOne">Collapsible Group Item</a>
      </h4>
    </div>
    <div class="panel-collapse collapse" id="collapseOne">
      <div class="panel-body">
        Content Goes here
      </div>
    </div>
  </div>
  <div class="panel panel-default">
    <div class="panel-heading">
      <h4 class="panel-title">
        <a class="" data-parent="#accordion" data-toggle="collapse" href=
        "#collapseTwo">Typography Variables</a>
      </h4>
    </div>
    <div class="panel-collapse collapse in" id="collapseTwo">
      <div class="panel-body">
        <h4>Try Something neat</h4>
        Content Goes here
      </div>
    </div>
  </div>
  <div class="panel panel-default">
    <div class="panel-heading">
      <h4 class="panel-title">
        <a class="collapsed" data-parent="#accordion" data-toggle=
        "collapse" href="#collapseThree">Easy Edit</a>
      </h4>
    </div>
    <div class="panel-collapse collapse" id="collapseThree">
      <div class="panel-body">
        Content Goes here
      </div>
    </div>
  </div>
</div>
```

