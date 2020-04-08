---
description: >-
  Sass is a CSS pre-processor, meaning that it extends the CSS language, adding
  features that allow variables, mixins, functions. Pages support Sass and is
  purely built on top of Sass
---

# Sass

Sass Files are found under `pages/src/sass`

* [sass](http://pages.revox.io/dashboard/3.0.0/docs/partials/sass.html#)
  * [modules](http://pages.revox.io/dashboard/3.0.0/docs/partials/sass.html#)
  * [themes](http://pages.revox.io/dashboard/3.0.0/docs/partials/sass.html#)
  * [mixin.scss](http://pages.revox.io/dashboard/3.0.0/docs/partials/sass.html#)
  * [modules.scss](http://pages.revox.io/dashboard/3.0.0/docs/partials/sass.html#)
  * [pages.scss](http://pages.revox.io/dashboard/3.0.0/docs/partials/sass.html#)
  * [responsive.scss](http://pages.revox.io/dashboard/3.0.0/docs/partials/sass.html#)

## **Modules**

The separation of modules help you to remove what's not necessary and build your own custom pages CSS

| NAME | DESCRIPTION |
| :--- | :--- |
| layout.scss | The core layout styles for pages |
| headers.scss | Top Navigation bar |
| respnsive.scss | The responsive handlers |
| cards.scss | Bootstrap cards over-written classes |
| chat.scss | Contains classes for the right hand sidebar chat |
| typography.scss | Contains all typo related styles included bg-color |
| button.scss | Bootstrap button over-written classes and pages dropdown |
| alerts.scss | Bootstrap alert messages over-written classes |
| breadcrumb.scss | Bootstrap breadcrumb classes |
| notifications.scss | Pages notifications, bootstrap badges, popovers |
| checkbox.scss | Pages checkboxes  |
| horizontal\_layout.scss | Pages horizontal layout classes for executive and casual layout |
| horizontal\_menu.scss | Horizontal dropdown menu |
| icons.scss | Pages icons |
| list.scss | iOS style listview in chat and email |
| progress\_indicators.scss | Pages progress bars, bootstrap native progress |
| modals.scss | Bootstrap Modal Classes |
| tabs\_accordian.scss | Bootstrap tabs and accordains |
| sliders.scss | Class for sliders |
| treeview.scss | Class for treeview |
| nestables.scss | Class for nestables |
| form\_elements.scss | All form related class including layouts & validations |
| tables.scss | Classes for bootstrap tables and datatables |
| tables.scss | Classes for bootstrap tables and datatables |
| vector\_map.scss | Classes for mapplic plugin |
| charts.scss | All chart related classes |
| print.scss | Print media query for invoice |
| overlay-search.scss | Pages quick search classes |
| quick-view.scss | Pages right hand-side quick drawer |
| lockscreen.scss | Class for lockscreen |
| page-loader.scss | PaceJS classes for page loading bar |
| calendar.scss | Pages Calendar plugin |
| social.scss | Pages Social |
| email.scss | Pages email |
| login.scss | Login page |
| misc.scss | All other utilities and helper classes |
| gallery.scss | Image gallery |
| z-index.scss | To maintain heierachchy and order for layers |

## **Variables**

Variables help to generate themes, you can custom build your very own theme. The variables will be included inside a specific theme e.g: scss/themes/default/var.scss by changing the few 5 main color variables you can create your color palette  


## **Creating your own Color Pallets**

By simply changing the following variables the entire color palette mention here will change Color Palette   
  
**Main Base color**   
`$color-contrast-lower  
$color-contrast-higher`

   
**Primary Colors**   
`$color-success`   
`$color-complete`   
`$color-primary`   
`$color-warning`   
`$color-danger`   
`$color-info`  


**Mixins**

We have made a wide variety of mixins that can be used in scss,   
mixins can be found under `pages/src/scss/mixin.scss`  


