# Select

pgSelect is a fork of[ NG-ZORRO](https://github.com/NG-ZORRO/ng-zorro-antd) implementation of select dropdown. Initial credits go to the author

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { pgSelectModule} from '../@pages/components/select/select.module';
@NgModule({
  imports: [pgSelectModule,...]
})
export class AppModule(){}
```

## How to use 

Basic Select with Search

{% tabs %}
{% tab title="HTML" %}
```markup
<pg-select style="width: 100%;" [(ngModel)]="selectedOption" [PlaceHolder]="'Select Option'" AllowClear ShowSearch>
    <pg-option
    *ngFor="let option of options"
    [Label]="option.label"
    [Value]="option"
    [Disabled]="option.disabled">
    </pg-option>
</pg-select>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
selectedOption;
options = [
{ value: 'jack', label: 'Jacks' },
{ value: 'lucy', label: 'Lucy' },
{ value: 'disabled', label: 'Disabled', disabled: true }
];
```
{% endtab %}
{% endtabs %}

## API

| parameter | Instructions | Types of | Defaults |
| :--- | :--- | :--- | :--- |
| SearchChange | Search content change callback function, parameter search content | Func | no |
| Mode | Set the Select mode | 'multiple' \| 'tags' | - |
| OpenChange | Drop-down menu opens close callback function | Func | no |
| Filter | Whether according to input filter options | Boolean | true |
| KeepUnListOptions | When this attribute is added, data that is not in the current selection box but has been selected will remain valid only for multiple selections | attribute | - |
| AllowClear | When this attribute is added, it supports clearing, and the radio mode is valid. | attribute | - |
| ScrollToBottom | The drop-down menu scrolls to the bottom callback, which can be used as a trigger for dynamic loading | - | - |
| PlaceHolder | Select box default text | String | no |
| ShowSearch | Whether to enable the search box | Boolean | false |
| NotFoundContent | What to display when the drop-down list is empty | String | 'Not Found' |

## Options API

| parameter | Instructions | Types of | Defaults |
| :--- | :--- | :--- | :--- |
| Label | Display option content for display | String |  |
| \#OptionTemplate | Used to customize the display of the drop-down section option | of-template |  |
| Disabled | Is it disabled | Boolean | false |

