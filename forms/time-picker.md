# Time Picker

pg-timepicker is a fork of[ NG-ZORRO](https://github.com/NG-ZORRO/ng-zorro-antd) implementation of Time Picker Initial credits go to the author

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { pgTimePickerModule } from '@pages/components/time-picker/timepicker.module';
@NgModule({
  imports: [pgTimePickerModule,...]
})
export class AppModule(){}
```

## How to use 

Basic Select with Search

{% tabs %}
{% tab title="HTML" %}
```markup
<pg-timepicker [(ngModel)]="_date"></pg-timepicker>
```
{% endtab %}
{% endtabs %}

## API

| parameter | Instructions | Types of | Defaults |
| :--- | :--- | :--- | :--- |
| of the Model | Default time | string or Date | no |
| PlaceHolder | The content displayed when there is no value | String | "Please select time" |
| Format | Displayed time format | String | "HH:mm:ss","HH:mm" |
| Disabled | Disable all actions | Boolean | false |
| DisabledHours | Prohibit selection of partial hours option | function\(\) | no |
| DisabledMinutes | Do not select partial minutes option | function\(selectedHour\) | no |
| DisabledSeconds | Disable selection of partial seconds | function\(selectedHour, selectedMinute\) | no |
| HideDisabledOptions | Add this property to hide forbidden options | attribute | - |

