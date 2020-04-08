# Grid

Bootstrap grid includes a responsive, mobile first fluid grid system that appropriately scales up to 12 columns as the device or viewport size increases. It includes predefined classes for easy layout options, as well as powerful mixins for generating more semantic layouts

## Introduction

Grid systems are used for creating page layouts through a series of rows and columns that house your content. Here's how the Bootstrap grid system works:

* You must start with `row`
* There are pre-define classes of columns starting from 1 to 12, example `col-md-1` to `col-md-12`
* Each of these value represent a percentage of the screen, 1 being the smallest and 12 being 100%
* You can create different grid pattern that finally forms 12

  eg :  


  ```markup
  <div class="row">
    <div class="col-md-1">.col-md-1</div>
    <div class="col-md-1">.col-md-1</div>
    <div class="col-md-1">.col-md-1</div>
    <div class="col-md-1">.col-md-1</div>
    <div class="col-md-1">.col-md-1</div>
    <div class="col-md-1">.col-md-1</div>
    <div class="col-md-1">.col-md-1</div>
    <div class="col-md-1">.col-md-1</div>
    <div class="col-md-1">.col-md-1</div>
    <div class="col-md-1">.col-md-1</div>
    <div class="col-md-1">.col-md-1</div>
    <div class="col-md-1">.col-md-1</div>
  </div>
  <div class="row">
    <div class="col-md-8">.col-md-8</div>
    <div class="col-md-4">.col-md-4</div>
  </div>
  <div class="row">
    <div class="col-md-4">.col-md-4</div>
    <div class="col-md-4">.col-md-4</div>
    <div class="col-md-4">.col-md-4</div>
  </div>
  <div class="row">
    <div class="col-md-6">.col-md-6</div>
    <div class="col-md-6">.col-md-6</div>
  </div>
  ```

* There different grids for different screen sizes, "col-md" md stands for medium screen, the following table explains  


  |  | `EXTRA SMALL DEVICES PHONES (<768PX)` | `SMALL DEVICESTABLETS (≥768PX)` | `MEDIUM DEVICESDESKTOPS (≥992PX)` | `LARGE DEVICESDESKTOPS (≥1200PX)` |
  | :--- | :--- | :--- | :--- | :--- |
  | `Grid behavior` | `Horizontal at all times` | `Collapsed to start, horizontal above breakpoints` |  |  |
  | `Container width` | `None (auto)` | `750px` | `970px` | `1170px` |
  | `Class prefix` | `.col-xs-` | `.col-sm-` | `.col-md-` | `.col-lg-` |
  | `# of columns` | `12` |  |  |  |
  | `Column width` | `Auto` | `~62px` | `~81px` | `~97px` |
  | `Gutter width` | `30px (15px on each side of a column)` |  |  |  |
  | `Nestable` | `Yes` |  |  |  |
  | `Offsets` | `Yes` |  |  |  |
  | `Column ordering` | `Yes` |  |  |  |

