# Content

Contents are referred to as inner layout structure. We have pre-build different inner content structures that are widely used for different web apps or even mobiles apps  


Layouts:

* Plain
* Coverpage with parallax
* Full height coverpage with parallax
* Page title parallax
* Column view 3:9
* Column view 9:3
* Column view 6:6

## **Plain**

```markup
<!-- START PAGE CONTENT -->
<div class="content">
    <!-- START PAGE COVER -->
    <div class="container-fluid container-fixed-lg ">
        <ul class="breadcrumb">
            <li>
                <p>home</p>
            </li>
            <li><a href="#" class="active">Plain template</a> 
            </li>
        </ul>
        <!-- END BREADCRUMB -->
        <h3 class="page-title">Page Title</h3>
    </div>

    <div class="container-fluid container-fixed-lg">

          <!-- CONTENT GOES HERE-->

    </div>
</div>
<!-- END PAGE CONTENT -->
```

## **Coverpage with parallax**

```markup
<div class="content">
  <!-- START JUMBOTRON -->
  <div class="jumbotron page-cover" data-pages="parallax">
    <div class="container-fluid container-fixed-lg">
      <div class="inner">
        <!-- START BREADCRUMB -->
        <ul class="breadcrumb">
          <li>
            <p>Home</p>
          </li>
          <li>
            <a class="active" href="#">Parrallax</a>
          </li>
        </ul><!-- END BREADCRUMB -->
        <div class="container-md-height m-b-20">
          <div class="row row-md-height">
            <div class="col-lg-7 col-md-6 col-md-height col-middle bg-white">
              <!-- START PANEL -->

              <div class="full-height">
                <div class="panel-body text-center">
                
                </div>
              </div><!-- END PANEL -->
            </div>

            <div class="col-lg-5 col-md-height col-md-6 col-top">
              <!-- START PANEL -->

              <div class="panel panel-transparent">
                <div class="panel-heading">
                  <div class="panel-title">
                    Getting started
                  </div>
                </div>

                <div class="panel-body">

                </div>
              </div><!-- END PANEL -->
            </div>
          </div>
        </div>
      </div>
    </div>
  </div><!-- END JUMBOTRON -->

  <div class="container-fluid container-fixed-lg ">

  </div>
</div><!-- END PAGE CONTENT -->
```

## **Full height coverpage with parallax**

```markup
<div class="page-content-wrapper content-builder full-height">
  <!-- START PAGE CONTENT -->
  <div class="content full-height">
    <!-- START JUMBOTRON -->
    <div class="jumbotron full-height no-padding" data-pages="parallax">
      <div class="container-fluid container-fixed-lg sm-p-l-20 sm-p-r-20 full-height">
        <div class="inner full-height">
          <div class="container-xs-height full-height">
            <div class="col-xs-height col-middle text-center">
              <div class="col-md-6 col-md-offset-3 text-center">
                <h2 class="text-center"><img alt="logo" src="assets/img/logo.png"> makes it super-easy to create your
                dashboard Without a designer.</h2><button class="btn btn-success btn-rounded">Live Preview</button>
                <button class="btn btn-link text-white">Watch Video</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div><!-- END JUMBOTRON -->

    <div class="container-fluid container-fixed-lg">
    
    </div>
  </div>
</div><!-- END PAGE CONTENT -->
```

## **Page title parallax**

```markup
<div class="content">
  <!-- START JUMBOTRON -->
  <div class="jumbotron no-margin" data-pages="parallax">
    <div class="container-fluid container-fixed-lg sm-p-l-20 sm-p-r-20">
      <div class="inner">
        <h3 class="">Page Title</h3>
      </div>
    </div>
  </div><!-- END JUMBOTRON -->
  <div class="container-fluid container-fixed-lg demo-container">
    <!-- START BREADCRUMB -->
    <ul class="breadcrumb">
      <li>
        <p>home</p>
      </li>
      <li>
        <a class="active" href="#">Parallax for page title</a>
      </li>
    </ul><!-- END BREADCRUMB -->
    
  </div>
</div><!-- END PAGE CONTENT -->
```

## **Column view 3:9**

```markup
<!-- START PAGE CONTENT WRAPPER -->
<div class="page-content-wrapper content-builder full-height">  
    <!-- START PAGE CONTENT -->
    <div class="content full-height">
        <div class="container-fluid full-height no-padding">
            <div class="row full-height no-margin">
                <div class="col-md-3 no-padding b-r b-grey sm-b-b full-height">
                    <div class="bg-white full-height">
                    <!-- YOU CAN REMOVE FULL-HEIGHT IN ALL PARENT ELEMENTS TO EXPEND TO CONTENT HEIGHT
                       YOU CAN ALSO CHANGE THE BACKGROUND COLOR BY ADDING THE BG CLASSES
                       EXAMPLE : bg-success
                     -->
                    </div>
                </div>
                <div class="col-md-9 no-padding full-height">
                    <div class="placeholder full-height">
                    <!-- YOU CAN REMOVE FULL-HEIGHT IN ALL PARENT ELEMENTS TO EXPEND TO CONTENT HEIGHT
                       YOU CAN ALSO CHANGE THE BACKGROUND COLOR BY ADDING THE BG CLASSES
                       EXAMPLE : bg-success
                     -->
                    </div>
                </div>
            </div>
            </div>
    </div>
    <!-- END PAGE CONTENT -->
</div>
<!-- END PAGE CONTENT WRAPPER -->
```

**Column view 9:3**

```markup
<!-- START PAGE CONTENT WRAPPER -->
<div class="page-content-wrapper content-builder full-height">  
    <!-- START PAGE CONTENT -->
    <div class="content full-height">
        <div class="container-fluid full-height no-padding">
            <div class="row full-height no-margin">
                <div class="col-md-9 no-padding b-r b-grey sm-b-b full-height">
                    <div class="bg-white full-height">
                    <!-- YOU CAN REMOVE FULL-HEIGHT IN ALL PARENT ELEMENTS TO EXPEND TO CONTENT HEIGHT
                       YOU CAN ALSO CHANGE THE BACKGROUND COLOR BY ADDING THE BG CLASSES
                       EXAMPLE : bg-success
                     -->
                    </div>
                </div>
                <div class="col-md-3 no-padding full-height">
                    <div class="placeholder full-height">
                    <!-- YOU CAN REMOVE FULL-HEIGHT IN ALL PARENT ELEMENTS TO EXPEND TO CONTENT HEIGHT
                       YOU CAN ALSO CHANGE THE BACKGROUND COLOR BY ADDING THE BG CLASSES
                       EXAMPLE : bg-success
                     -->
                    </div>
                </div>
            </div>
            </div>
    </div>
    <!-- END PAGE CONTENT -->
</div>
<!-- END PAGE CONTENT WRAPPER -->
```

**Column view 6:6**

```markup
<!-- START PAGE CONTENT WRAPPER -->
<div class="page-content-wrapper content-builder full-height">  
    <!-- START PAGE CONTENT -->
    <div class="content full-height">
        <div class="container-fluid full-height no-padding">
            <div class="row full-height no-margin">
                <div class="col-md-6 no-padding b-r b-grey sm-b-b full-height">
                    <div class="bg-white full-height">
                    <!-- YOU CAN REMOVE FULL-HEIGHT IN ALL PARENT ELEMENTS TO EXPEND TO CONTENT HEIGHT
                       YOU CAN ALSO CHANGE THE BACKGROUND COLOR BY ADDING THE BG CLASSES
                       EXAMPLE : bg-success
                     -->
                    </div>
                </div>
                <div class="col-md-6 no-padding full-height">
                    <div class="placeholder full-height">
                    <!-- YOU CAN REMOVE FULL-HEIGHT IN ALL PARENT ELEMENTS TO EXPEND TO CONTENT HEIGHT
                       YOU CAN ALSO CHANGE THE BACKGROUND COLOR BY ADDING THE BG CLASSES
                       EXAMPLE : bg-success
                     -->
                    </div>
                </div>
            </div>
            </div>
    </div>
    <!-- END PAGE CONTENT -->
</div>
<!-- END PAGE CONTENT WRAPPER -->
```

