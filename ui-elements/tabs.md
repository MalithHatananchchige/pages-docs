# Tabs

Tabs are created using Bootstrap Native Tabs, they will work as the same way how it works in bootstrap, but it is styled to pages color scheme.To add a Tabs to pages please refer following guidelines

{% embed url="https://getbootstrap.com/docs/4.1/components/navs/\#tabs" caption="Bootstrap Documentation" %}

## **Creating a Tab**

Place this HTML code in any "Pages" html file ****

{% hint style="info" %}
**Tip : Tabs**   
Make sure you keep the tab pane ID's unique
{% endhint %}

```markup
<div class="panel">
  <ul class="nav nav-tabs nav-tabs-simple">
    <li class="active">
      <a data-toggle="tab" href="#tab2hellowWorld">Hello World</a>
    </li>
    <li>
      <a data-toggle="tab" href="#tab2FollowUs">Hello Two</a>
    </li>
    <li>
      <a data-toggle="tab" href="#tab2Inspire">Hello Three</a>
    </li>
  </ul>
  <div class="tab-content">
    <div class="tab-pane active" id="tab2hellowWorld">
      <div class="row column-seperation">
        <div class="col-md-6">
          <h3>
            <span class="semi-bold">Sometimes</span> Small things in life means
            the most
          </h3>
        </div>
        <div class="col-md-6">
          <h3 class="semi-bold">
            great tabs
          </h3>
          <p>
            Native boostrap tabs customized to Pages look and feel, simply
            changing class name you can change color as well as its animations
          </p>
        </div>
      </div>
    </div>
    <div class="tab-pane" id="tab2FollowUs">
      <div class="row">
        <div class="col-md-12">
          <h3>
            “ Nothing is <span class="semi-bold">impossible</span>, the word
            itself says 'I'm <span class="semi-bold">possible</span>'! ”
          </h3>
          <p>
            A style represents visual customizations on top of a layout. By
            editing a style, you can use Squarespace's visual interface to
            customize your...
          </p><br>
          <p class="pull-right">
            <button class="btn btn-white btn-cons" type="button">White</button>
            <button class="btn btn-success btn-cons" type=
            "button">Success</button>
          </p>
        </div>
      </div>
    </div>
    <div class="tab-pane" id="tab2Inspire">
      <div class="row">
        <div class="col-md-12">
          <h3>
            Follow us &amp; get updated!
          </h3>
          <p>
            Instantly connect to what's most important to you. Follow your
            friends, experts, favorite celebrities, and breaking news.
          </p><br>
        </div>
      </div>
    </div>
  </div>
</div>
```

## **Tab Orientation**

To change tab orientation, create a tab like before using the above code, add the class `nav-tabs-left` or `nav-tabs-left`to `nav nav-tabs` UL element

```markup
<!-- LEFT ORIENTATION -->
<div class="panel">
  <ul class="nav nav-tabs nav-tabs-left nav-tabs-simple">
  ....
  </ul>
  <div class="tab-content">
  ....
  </div>
</div>

<!-- RIGHT ORIENTATION -->
<div class="panel">
  <ul class="nav nav-tabs nav-tabs-right nav-tabs-simple">
  ....
  </ul>
  <div class="tab-content">
  ....
  </div>
</div>
```

## **Tab Styles**

To change tab styles, create a tab like before using the first code in **Create Tab section**, add the class `nav-tabs-linetriangle` or `nav-tabs-fillup` to `nav nav-tabs` UL element ****

{% hint style="info" %}
**Tip : Tabs**  
You can try different orientation with tab styles
{% endhint %}

```markup
<!-- LINE TRIANGLE -->
<div class="panel">
  <ul class="nav nav-tabs nav-tabs-linetriangle nav-tabs-simple">
  ....
  </ul>
  <div class="tab-content">
  ....
  </div>
</div>

<!-- FILL UP ANIMATION -->
<div class="panel">
  <ul class="nav nav-tabs nav-tabs-fillup nav-tabs-simple">
  ....
  </ul>
  <div class="tab-content">
  ....
  </div>
</div>
```

## **Sliding Tabs**

Append `slide-left` or `slide-right` to `tab-pane` to reveal tab content with a sliding effect

```markup
<!-- Nav tabs -->
<ul class="nav nav-tabs">
    <li class="active">
        <a data-toggle="tab" href="#slide1">
            <span>Home</span>
        </a>
    </li>
    <li>
        <a data-toggle="tab" href="#slide2">
            <span>Profile</span>
        </a>
    </li>
</ul>
<!-- Tab panes -->
<div class="tab-content">
    <div class="tab-pane slide-left active" id="slide1">
        ...
    </div>
    <div class="tab-pane slide-right" id="slide2">
        ...
    </div>
</div>
```

## **Responsive Tabs**

Responsive tabs are not built on to bootstrap by default, We have integrated 3 options to choose from



