---
description: >-
  Welcome to Rails Pages Gem. The following will not install all thirdparty
  dependencies used in the demo. It has to be installed later manually.
---

# Rails

## **Installation**

Add this line to your application's Gemfile:

```text
gem 'pages-rails','3.0.0',:git => 'https://github.com/revoxltd/pages-rails.git'
```

Install from branch/tag/release

```text
gem 'pages-rails', :git => "https://github.com/revoxltd/pages-rails.git", :ref => "4aded"
gem 'pages-rails', :git => "https://github.com/revoxltd/pages-rails.git", :branch => "2-3-stable"
gem 'pages-rails', :git => "https://github.com/revoxltd/pages-rails.git", :tag => "v2.3.5"
```

And then execute:

```text
$ bundle
```

Or install it yourself as:

```text
$ gem install pages-rails
```

## **Usage**

1. Add to your application.js Will Include core pages.js

```text
//= require pages
```

Adding other components like calendar,email etc

```text
//= require pages.calendar
//= require pages.email
//= require pages.social
```

1. Add to your application.scss or to your custom.scss file

```text
$base-img-url: "/assets";
@import "pages";
```

You can update varriables as you wish. To see the varriables used open the file stylesheets/\_var.scss [Click here](https://github.com/revoxltd/pages-rails/blob/master/vendor/assets/stylesheets/_var.scss)

```text
$color-master: #626262 !default;
```

You should add varriables before

```text
@import "pages";
```

You could also require specific module per page eg:

```text
$base-img-url: "/assets";
@import "modules/_layouts";
@import "modules/_modals";
```

Include theme \(dont include with pages.rtl or pages, only include the following\)

```text
$base-img-url: "/assets";
@import "themes/calendar";
```

## Dependencies

| PLUGIN | DESCRIPTION | DEP. STATUS |
| :--- | :--- | :--- |
| jquery.js | Core JS Library | **REQUIRED** |
| mordnerizer.js | Browser Feature Detection | **REQUIRED** |
| bootstrap.js | Core Framework | **REQUIRED** |
| pace.js | Page Progress Loader | **OPTIONAL** |
| jquery-unviel.js | Library Used for displaying retina images | **OPTIONAL** |
| jquery-bez.js | Sidebar Animation Lib for IE9 | **OPTIONAL** |
| jquery.ioslist.js | Used Chat list on the quickview | **OPTIONAL** |
| jquery.actual.js | Determine image dimentions | **OPTIONAL** |
| jquery.scrollbar.js | Scrollbar plugin used in sidebar and portlets | **OPTIONAL** |

{% page-ref page="rails.md" %}



