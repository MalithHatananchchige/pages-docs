---
description: >-
  Pre-built widget components that you can integrate with your dashboards or
  social feeds.
---

# Widgets

Pages comes with 24 pre-built widget components that you can easily integrate with your dashboards in no time. These can be found in `dashboard/widgets`folder and each widget folder is named after its `@Component`'s `selector.`Widgets are based off [pgcard component](ui-components/cards.md) 

## Importing

Widgets are available throughout all the pre-built dashboards via `dashboard.module.ts`. But if you are planning use them outside you will have to import them as below. 

```typescript
// Using ImageWidgetComponent as an example. Same steps apply to other widgets
import { ImageWidgetComponent } from './widgets/image-widget/image-widget.component';
@NgModule({
  declarations: [ImageWidgetComponent,...]
})
export class AppModule(){}
```

## bar-tile-widget

Features a stacked bar chart made with `echarts` component:

```http
<bar-tile-widget></bar-tile-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.49.14-pm.png)

## graph-live-widget

Features a looping vertical slider with stock market updates. 

```http
<graph-live-widget></graph-live-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.49.56-pm.png)

## graph-options-widget

Features a line chart with toggle buttons. 

```http
<graph-options-widget></graph-options-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.50.44-pm.png)

## graph-tile-flat-widget

Features a line chart with sales stats. 

```http
<graph-tile-flat-widget></graph-tile-flat-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.48.40-pm%20%281%29.png)

## graph-tile-widget

Features a line chart with area filled in. 

```http
<graph-tile-widget></graph-tile-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.48.28-pm.png)

## graph-widget

Features a line chart with multiple series of data.

```http
<graph-widget></graph-widget>
```

| **Property** | **Description** | **Type** | **Default** |
| :--- | :--- | :--- | :--- |
| `IsAlt` | Toggles three boxes with stock trading highlights and a search bar | boolean | false |

![](.gitbook/assets/screen-shot-2018-06-03-at-3.07.36-pm.png)

![Default view](.gitbook/assets/screen-shot-2018-06-03-at-1.49.23-pm.png)

## image-widget

Features a background image and an text overlay. 

```http
<image-widget></image-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.47.50-pm.png)

## image-widget-basic

Features a background image and a text overlay. Intended to use for showing minimal content. 

```http
<image-widget-basic></image-widget-basic>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.49.34-pm.png)

## plain-live-widget

Features a rotating text

```http
<plain-live-widget></plain-live-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.49.41-pm.png)

## plain-widget

Features quick weather info 

```http
<plain-widget></plain-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.49.49-pm.png)

## progress-tile-flat-widget

Features a large title text and a progress bar

```http
<progress-tile-flat-widget></progress-tile-flat-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.48.52-pm.png)

## project-progress-widget

Features multiple progress bars in a tab view. 

```http
<project-progress-widget></project-progress-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.54.34-pm.png)

## quick-stats-widget

Features quick stats in extra large text and a progress bar.

```http
<quick-stats-widget></quick-stats-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-3.13.52-pm.png)

## realtime-widget

Designed to show live streaming data in a line chart. Demo widget represents sample data updated using a timer. 

```http
<realtime-widget></realtime-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.50.20-pm.png)

## social-image-tile-widget

Shows an image in the style of a social feed post. 

```http
<social-image-tile-widget></social-image-tile-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-8.05.24-pm.png)

## social-post-tile-widget

Shows a social post with text and an image. 

```http
<social-post-tile-widget></social-post-tile-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-8.05.31-pm.png)

## stacked-bar-widget

Features a [pg-tabset](ui-components/tabs.md) component with stacked bar charts representing multiple data sources for quick comparison.  

```http
<stacked-bar-widget></stacked-bar-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.50.31-pm.png)

## stat-tile-widget

This is also another mini widget similar to `quick-stats-widget` and `progress-tile-flat widget`. Sample widget illustrates stock trading stats  

```http
<stat-tile-widget></stat-tile-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.49.01-pm.png)

## table-basic-widget

Features a basic table layout.  

```http
<table-basic-widget></table-basic-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.50.11-pm.png)

## table-widget

This is another variation of `table-basic-widget.` 

```http
<table-widget></table-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-8.40.20-pm.png)

## todo-list-widget

Show todo-list items with checkboxes. 

```http
<todo-list-widget></todo-list-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-1.54.42-pm.png)

## weather-widget

Shows weekly weather data together with animated weather icons from [Skycons](https://github.com/darkskyapp/skycons). 

```http
<todo-list-widget></todo-list-widget>
```

| **Property** | **Description** | **Type** | **Default** |
| :--- | :--- | :--- | :--- |
| `Type` | By default weather widget shows two highlighted columns with weather data to the right in extra large screens. Set this to "compact" to disable them.  | string | undefined |

![With Type option set to &quot;compact&quot;](.gitbook/assets/screen-shot-2018-06-03-at-1.50.50-pm.png)

![Default widget](.gitbook/assets/screen-shot-2018-06-03-at-8.51.45-pm.png)

## weekly-sales-widget

This is also another mini widget showing weekly sales data.  

```http
<weekly-sales-widget></weekly-sales-widget>
```

![](.gitbook/assets/screen-shot-2018-06-03-at-8.54.50-pm.png)

