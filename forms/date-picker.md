# Date Picker

pg-datepicker is a fork of[ NG-ZORRO](https://github.com/NG-ZORRO/ng-zorro-antd) implementation of Date / Date Range Picker Initial credits go to the author

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { pgDatePickerModule } from '@pages/components/datepicker/datepicker.module';
@NgModule({
  imports: [pgDatePickerModule,...]
})
export class AppModule(){}
```

## How to use 

Basic Select with Search

{% tabs %}
{% tab title="HTML" %}
```markup
<div class="input-group date col-md-8 p-l-0">
  <pg-datepicker></pg-datepicker>
  <div class="input-group-append">
      <span class="input-group-text">
        <i class="fa fa-calendar"></i>
      </span>
  </div>
</div>
```
{% endtab %}
{% endtabs %}

## API

The date class component includes the following three forms.

* pg-datepicker
* pg-datepicker \[Mode='month'\]
* pg-rangepicker

#### Common API

| parameter | Instructions | Types of | Defaults |
| :--- | :--- | :--- | :--- |
| Format | Display date format, configuration reference [Moment.js documentation](http://momentjs.cn/docs/#/parsing/string-formats/) | String | "YYYY-MM-DD" |
| Disabled | Disabled | boolean | false |
| AllowClear | Whether to show clear button | boolean | true |
| ShowTime | Time options, see nz-timepicker parameter | boolean \| TimePickerInnerComponent | null |
| DisabledDate | A callback function to disable the date, returning true to disable this date | \(Date\) =&gt; boolean |  |

#### pg-datepicker

| parameter | Instructions | Types of | Defaults |
| :--- | :--- | :--- | :--- |
| Model | Display date | Date | Current date |
| Placeholder | Input box prompt text | String |  |
| Mode | Selector mode, `month`select only to month, `day`select to day | String | "day" |

#### pg-rangepicker

| parameter | Instructions | Types of | Defaults |
| :--- | :--- | :--- | :--- |
| Model | Display date | \[Date, Date\] | Current date |
| Placeholder | Input box prompt text | \[String, String\] |  |

