# Views

## **Basic HTML Tag Structure**

The below code is a basic structure for a view to work, you need to have all your `view` wrapped in a `view-port`

```markup
 <!-- BEGIN View Port !-->
 <div class="view-port clearfix" id="myViewPort">
  <!-- BEGIN View !-->
  <div class="view bg-white">

  </div>
  <!-- END View !-->

  <!-- BEGIN View !-->
  <div class="view bg-white">

  </div>
  <!-- END View !-->
 </div>
 <!-- END View Port !-->
```

### **How to Navigate**

You can navigate with a simple HTML link and the following attributes in it

```markup
<a data-view-animation="push-parrallax" data-view-port="#myViewPort" data-navigate="view" class="" href="#">
Go to View
</a>
```

  
`data-view-animation` : Defines animation - push-parrallax / push / from-top   
  
`data-view-port` : Defines Parent View Port - ID of parent view port. Eg : "\#myViewPort"   
  
`data-navigate` : Enables to toggle back and forth form two views in a view port   
  


## **One to Many Navigation**

There is an option where you can navigate from one view to different views, the structure will be the following  


**HTML**

```markup
 <!-- BEGIN View Port !-->
 <div class="view-port clearfix" id="myViewPort">
  <!-- BEGIN View !-->
  <div class="view bg-white">

  </div>
  <!-- END View !-->

  <!-- BEGIN View !-->
  <div class="view bg-white">
    <div class="view bg-white" id="subView1">
      Your Content One
    </div>
    <div class="view bg-white" id="subView2">
      Your Content Two
    </div>
  </div>
  <!-- END View !-->
 </div>
 <!-- END View Port !-->
```

**Link**

To link to the subview add the attribute called `data-toggle-view` this defines the ID of your subview

```markup
<a data-view-animation="push-parrallax" data-view-port="#myViewPort" data-navigate="view" data-toggle-view="#subView1" class="" href="#">
Go to View
</a>
```

## **Multi Level Navigation**

You can navigate up to unlimited levels by nesting views-ports under `views`  


**HTML Structure**

```markup
 <!-- BEGIN View Port !-->
 <div class="view-port clearfix" id="myViewPort">
  <!-- BEGIN View !-->
  <div class="view bg-white">
    Your Content
  </div>
  <!-- END View !-->

  <!-- BEGIN View !-->
  <div class="view bg-white">
     <!-- BEGIN View Port !-->
     <div class="view-port clearfix" id="myNestedViewPort">
      <!-- BEGIN View !-->
      <div class="view bg-white">
        Level One
      </div>
      <!-- END View !-->

      <!-- BEGIN View !-->
      <div class="view bg-white">
        Level Two
      </div>
      <!-- END View !-->
     </div>
     <!-- END View Port !-->
  </div>
  <!-- END View !-->
 </div>
 <!-- END View Port !-->
```

**Sample with Navigation Links**

```markup
<div class="view-port clearfix" id="myViewPort">
    <!-- BEGIN View !-->

    <div class="view bg-white">
        <a class="" data-navigate="view" data-view-animation="push-parrallax"
        data-view-port="#myViewPort" href="#">Go To Level One</a>
    </div><!-- END View !-->
    <!-- BEGIN View !-->

    <div class="view bg-white">
        <!-- BEGIN View Port !-->

        <div class="view-port clearfix" id="myNestedViewPort">
            <!-- BEGIN View !-->

            <div class="view bg-white">
                <p>Level One</p><br>
                <a class="" data-navigate="view" data-view-animation=
                "push-parrallax" data-view-port="#myNestedViewPort" href="#">Go
                To Level Two</a> <a class="" data-navigate="view"
                data-view-animation="push-parrallax" data-view-port=
                "#myViewPort" href="#">Go Back</a>
            </div><!-- END View !-->
            <!-- BEGIN View !-->

            <div class="view bg-white">
                <p>Level Two</p><br>
                <a class="" data-navigate="view" data-view-animation=
                "push-parrallax" data-view-port="#myNestedViewPort" href="#">Go
                Back</a>
            </div><!-- END View !-->
        </div><!-- END View Port !-->
    </div><!-- END View !-->
</div><!-- END View Port !-->
```

