# Form Wizard

Pages uses Bootstrap Wizard plugin to build a wizard out of a formatter tabable structure. It allows to build a wizard functionality using buttons to go through the different wizard steps and using events allows to hook into each step individually.

{% hint style="info" %}
Please refer to [Twitter Bootstrap Wizard Documentation](http://vadimg.com/twitter-bootstrap-wizard-example/) to learn about plugin options
{% endhint %}

**Step one**

Include the plugin javascript file inside the `<body>`before core template script inclusions, if it's not there already. Please view [jQuery plugin inclusion guideline rules](http://pages.revox.io/dashboard/3.0.0/docs/partials/js_rules.html)

```markup
<script type="text/javascript" src="assets/plugins/boostrap-form-wizard/js/jquery.bootstrap.wizard.min.js"></script>
```

**Step two**

Add the markup. It is recommended that you use `.nav-tabs-linetriangle` and `.nav-tabs-separator` with `.nav-tabs`. To make the tabs slide in, add `.slide` to each `.tab-pane`

```markup
<div id="myFormWizard">
    <!-- Nav tabs -->
    <ul class="nav nav-tabs nav-tabs-linetriangle nav-tabs-separator">
        <li class="active">
            <a data-toggle="tab" href="#tab1"><i class="fa fa-shopping-cart tab-icon"></i> <span>Your cart</span></a>
        </li>
        <li class="">
            <a data-toggle="tab" href="#tab2"><i class="fa fa-truck tab-icon"></i> <span>Shipping information</span></a>
        </li>
        <li class="">
            <a data-toggle="tab" href="#tab3"><i class="fa fa-credit-card tab-icon"></i> <span>Payment details</span></a>
        </li>
        <li class="">
            <a data-toggle="tab" href="#tab4"><i class="fa fa-check tab-icon"></i> <span>Summary</span></a>
        </li>
    </ul>
    <!-- Tab panes -->
    <div class="tab-content">
        <div class="tab-pane active slide" id="tab1">
            ...
        </div>
        <div class="tab-pane slide" id="tab2">
            ...
        </div>
        <div class="tab-pane slide" id="tab3">
            ...
        </div>
        <div class="tab-pane slide" id="tab4">
            ...
        </div>

        <ul class="pager wizard">
            <li class="next">
                <button class="btn btn-primary btn-cons btn-animated from-left fa fa-truck pull-right" type="button">
                    <span>Next</span>
                </button>
            </li>
            <li class="next finish" style="display:none;">
                <button class="btn btn-primary btn-cons btn-animated from-left fa fa-cog pull-right" type="button">
                    <span>Finish</span>
                </button>
            </li>
            <li class="previous first" style="display:none;">
                <button class="btn btn-white btn-cons btn-animated from-left fa fa-cog pull-right" type="button">
                    <span>First</span>
                </button>
            </li>
            <li class="previous">
                <button class="btn btn-white btn-cons pull-right" type="button">
                    <span>Previous</span>
                </button>
            </li>
        </ul>

        <div class="wizard-footer padding-20 bg-master-light">
            Copyright &copy; 2014 - Revox
        </div>
    </div>
</div>
```

**Step three**

Apply the plugin.

```markup
<script>
$(document).ready(function() {
    $('#myFormWizard').bootstrapWizard({
        onTabShow: function(tab, navigation, index) {
            var $total = navigation.find('li').length;
            var $current = index + 1;

            // If it's the last tab then hide the last button and show the finish instead
            if ($current >= $total) {
                $('#myFormWizard').find('.pager .next').hide();
                $('#myFormWizard').find('.pager .finish').show();
                $('#myFormWizard').find('.pager .finish').removeClass('disabled');
            } else {
                $('#myFormWizard').find('.pager .next').show();
                $('#myFormWizard').find('.pager .finish').hide();
            }

            var li = navigation.find('li.active');

            var btnNext = $('#myFormWizard').find('.pager .next').find('button');
            var btnPrev = $('#myFormWizard').find('.pager .previous').find('button');

            // remove fontAwesome icon classes
            function removeIcons(btn) {
                btn.removeClass(function(index, css) {
                    return (css.match(/(^|\s)fa-\S+/g) || []).join(' ');
                });
            }

            if ($current > 1 && $current < $total) {

                var nextIcon = li.next().find('.fa');
                var nextIconClass = nextIcon.attr('class').match(/fa-[\w-]*/).join();

                removeIcons(btnNext);
                btnNext.addClass(nextIconClass + ' btn-animated from-left fa');

                var prevIcon = li.prev().find('.fa');
                var prevIconClass = prevIcon.attr('class').match(/fa-[\w-]*/).join();

                removeIcons(btnPrev);
                btnPrev.addClass(prevIconClass + ' btn-animated from-left fa');
            } else if ($current == 1) {
                // remove classes needed for button animations from previous button
                btnPrev.removeClass('btn-animated from-left fa');
                removeIcons(btnPrev);
            } else {
                // remove classes needed for button animations from next button
                btnNext.removeClass('btn-animated from-left fa');
                removeIcons(btnNext);
            }
        }
    });
});
</script>
```

