# Sliders

pgSliders is a fork of[ NG-ZORRO](https://github.com/NG-ZORRO/ng-zorro-antd) implementation of drag slider. Initial credits go to the author

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { pgSliderModule } from '../@pages/components/slider/slider.module';
@NgModule({
  imports: [pgSliderModule,...]
})
export class AppModule(){}
```

## How to use 

Basic Slider with tooltip

{% tabs %}
{% tab title="HTML" %}
```markup
<pg-slider [DefaultValue]="30" Tooltip="true" TooltipForceVisiblity="true"></pg-slider>
```
{% endtab %}
{% endtabs %}

## API

| parameter | Description | Types of | Defaults |
| :--- | :--- | :--- | :--- |
| Range | Start the double slider mode when adding this property | attribute | - |
| Min | Minimum value | Number | 0 |
| Max | Maximum | Number | 100 |
| Step | Step size. The value must be greater than 0 and can be divisible by \(max - min\). When `marks`when the object is not empty, can be set `step`to `null`use this option only marks Slider values marked out portion. | Number | 1 |
| Marks | Tick ​​mark. key must be of type `number`and value in the closed interval \[min, max\] within, each tab may be provided separately style. | object | { number: string\|HTML } or { number: { style: object, label: string\|HTML } } |
| Dots | Whether it can only be dragged onto the scale | Boolean | false |
| of the Model | Set/get the current value. When `range`is `false`, the use `number`, or use`[number, number]` | number\|number\[\] |  |
| DefaultValue | Set the initial value. When `range`is `false`, the use `number`, or use`[number, number]` | number\|number\[\] | 0 or \[0, 0\] |
| Included | Whether it is included. `marks`Valid when not empty, when the value is true, the value is inclusive, and false is juxtaposed. | Boolean | true |
| Disabled | Whether to disable. Value `true`, the slider is disabled | Boolean | false |
| Vertical | Display vertically. When this property is added, the Slider is in the vertical direction. | attribute | - |
| OnAfterChange | And `onmouseup`consistent with the timing of the trigger, the current value as an argument. | Function\(value\) | no |
| TipFormatter | Slider will pass the current value `TipFormatter`, and `Tooltip`display `TipFormatter`the return value, if it is `null`, is hidden `Tooltip`. | Function\(value\) \| null | \(value\) =&gt; value |

