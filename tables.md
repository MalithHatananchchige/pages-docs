# Tables

## Basic **Tables**

Pages extensively uses Bootstrap's `.table` to style its tables. 

{% hint style="info" %}
Please refer to their documentation for guidelines. [Bootstrap Tables](http://getbootstrap.com/css/#tables)
{% endhint %}

## **DataTables**

DataTables is a highly flexible jQuery plug-in based upon the foundations of progressive enhancement, and will add advanced interaction controls to any HTML table.

{% hint style="info" %}
Please refer to [DataTables Documentation](http://www.datatables.net/) to learn about plugin options
{% endhint %}

**Step one**

Include the plugin stylesheet `jquery.dataTables.css` and other extensions inside the `<head>`. Please view [Stylesheet inclusion guideline rules](http://pages.revox.io/dashboard/3.0.0/docs/partials/)

```markup
<link type="text/css" rel="stylesheet" href="assets/plugins/jquery-datatable/media/css/jquery.dataTables.css">
<link type="text/css" rel="stylesheet" href="assets/plugins/jquery-datatable/extensions/FixedColumns/css/dataTables.fixedColumns.min.css">
<link media="screen" type="text/css" rel="stylesheet" href="assets/plugins/datatables-responsive/css/datatables.responsive.css">
```

**Step two**

Include the plugin javascript and extension files inside the `<body>`before core template script inclusions, if it's not there already.

```markup
<script type="text/javascript" src="assets/plugins/jquery-datatable/media/js/jquery.dataTables.min.js">
<script type="text/javascript" src="assets/plugins/jquery-datatable/extensions/TableTools/js/dataTables.tableTools.min.js">
<script type="text/javascript" src="assets/plugins/jquery-datatable/extensions/Bootstrap/jquery-datatable-bootstrap.js">
<script src="assets/plugins/datatables-responsive/js/datatables.responsive.js" type="text/javascript">
<script src="assets/plugins/datatables-responsive/js/lodash.min.js" type="text/javascript">
```

**Step three**

Create the markup for your table. You can also add [Bootstrap table classes](http://getbootstrap.com/css/#tables) to customize the look

```markup
<table id="myDataTable" class="table table-hover" cellspacing="0" width="100%">
    <thead>
        <tr>
            <th>Name</th>
            <th>Position</th>
            <th>Office</th>
            <th>Age</th>
            <th>Start date</th>
            <th>Salary</th>
        </tr>
    </thead>

    <tfoot>
        <tr>
            <th>Name</th>
            <th>Position</th>
            <th>Office</th>
            <th>Age</th>
            <th>Start date</th>
            <th>Salary</th>
        </tr>
    </tfoot>

    <tbody>
        <tr>
            <td>Tiger Nixon</td>
            <td>System Architect</td>
            <td>Edinburgh</td>
            <td>61</td>
            <td>2011/04/25</td>
            <td>$320,800</td>
        </tr>
        <tr>
            <td>Garrett Winters</td>
            <td>Accountant</td>
            <td>Tokyo</td>
            <td>63</td>
            <td>2011/07/25</td>
            <td>$170,750</td>
        </tr>
        <tr>
            <td>Ashton Cox</td>
            <td>Junior Technical Author</td>
            <td>San Francisco</td>
            <td>66</td>
            <td>2009/01/12</td>
            <td>$86,000</td>
        </tr>
        <tr>
            <td>Cedric Kelly</td>
            <td>Senior Javascript Developer</td>
            <td>Edinburgh</td>
            <td>22</td>
            <td>2012/03/29</td>
            <td>$433,060</td>
        </tr>
        <tr>
            <td>Airi Satou</td>
            <td>Accountant</td>
            <td>Tokyo</td>
            <td>33</td>
            <td>2008/11/28</td>
            <td>$162,700</td>
        </tr>
        <tr>
            <td>Brielle Williamson</td>
            <td>Integration Specialist</td>
            <td>New York</td>
            <td>61</td>
            <td>2012/12/02</td>
            <td>$372,000</td>
        </tr>
    </tbody>
</table>
```

**Step four**

Apply the plugin to your table.

```markup
<script>
$(document).ready(function() {
     $('#myDataTable').DataTable();
});
</script>
```

  
Use any of the following pre-configured settings to get DataTables customized to match your purpose. For more advanced options please refer to [DataTables Documentation](http://datatables.net/)

### **Table with a search box**

```markup
<!-- Markup -->
<input type="text" id="search-table" class="form-control pull-right" placeholder="Search">

<table class="table" id="tableWithSearch">
    ...
</table>

<!-- Apply the plugin -->
<script>
var table = $('#tableWithSearch');

var settings = {
    "sDom": "<'table-responsive't><'row'<p i>>",
    "sPaginationType": "bootstrap",
    "destroy": true,
    "scrollCollapse": true,
    "oLanguage": {
        "sLengthMenu": "_MENU_ ",
        "sInfo": "Showing <b>_START_ to _END_</b> of _TOTAL_ entries"
    },
    "iDisplayLength": 5
};

table.dataTable();

// search box for table
$('#search-table').keyup(function() {
    table.fnFilter($(this).val());
});
</script>
```

### **Table with dynamic rows**

```markup
<!-- Markup -->
<button id="add-row" type="button" class="btn btn-primary">Add New Row</button>

<table class="table" id="tableWithDynamicRows">
    <thead>
        <tr>
            <th style="width:25%">Column 1</th>
            <th style="width:30%">Column 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Hello</td>
            <td>there!</td>
        </tr>
    </tbody>
</table>

<!-- Apply the plugin -->
<script>
var table = $('#tableWithDynamicRows');

var settings = {
    "sDom": "<'table-responsive't><'row'<p i>>",
    "sPaginationType": "bootstrap",
    "destroy": true,
    "scrollCollapse": true,
    "oLanguage": {
        "sLengthMenu": "_MENU_ ",
        "sInfo": "Showing <b>_START_ to _END_</b> of _TOTAL_ entries"
    },
    "iDisplayLength": 5
};

table.dataTable(settings);

$('#add-row').click(function() {
    table.dataTable().fnAddData([
        "Foo",
        "Bar"
    ]);
});
</script>
```

### **Table with export options**

```markup
<!-- Markup -->
<div class="export-options-container"></div>
<table class="table" id="tableWithExportOptions">
    ...
</table>

<!-- Apply the plugin -->
<script>
var table = $('#tableWithExportOptions');

var settings = {
    "sDom": "<'exportOptions'T><'table-responsive't><'row'<p i>>",
    "sPaginationType": "bootstrap",
    "destroy": true,
    "scrollCollapse": true,
    "oLanguage": {
        "sLengthMenu": "_MENU_ ",
        "sInfo": "Showing <b>_START_ to _END_</b> of _TOTAL_ entries"
    },
    "iDisplayLength": 5,
    "oTableTools": {
        "sSwfPath": "assets/plugins/jquery-datatable/extensions/TableTools/swf/copy_csv_xls_pdf.swf",
        "aButtons": [{
            "sExtends": "csv",
            "sButtonText": "<i class='pg-grid'></i>",
        }, {
            "sExtends": "xls",
            "sButtonText": "<i class='fa fa-file-excel-o'></i>",
        }, {
            "sExtends": "pdf",
            "sButtonText": "<i class='fa fa-file-pdf-o'></i>",
        }, {
            "sExtends": "copy",
            "sButtonText": "<i class='fa fa-copy'></i>",
        }]
    },
    fnDrawCallback: function(oSettings) {
        $('.export-options-container').append($('.exportOptions'));
    }
};
table.dataTable(settings);
</script>
```

