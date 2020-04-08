# Select FX

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { pgSelectfx } from '../@pages/components/cs-select/select.module';
@NgModule({
  imports: [pgSelectfx,...]
})
export class AppModule(){}
```

## How to use 

Basic Select with Search

{% tabs %}
{% tab title="HTML" %}
```markup
<pg-select-fx style="width: 110px" [(ngModel)]="selectedOptionCS" [PlaceHolder]="'Select'" AllowClear>
    <pg-selectfx-option
    *ngFor="let option of csoptions"
    [Label]="option.label"
    [Value]="option"
    [Disabled]="option.disabled">
    </pg-selectfx-option>
</pg-select-fx>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
csoptions = [
    { value: 'Web-safe', label: 'Web-safe' },
    { value: 'Helvetica', label: 'Helvetica' },
    { value: 'SegeoUI', label: 'SegeoUI' }
];
selectedOptionCS;
```
{% endtab %}
{% endtabs %}

## API

| parameter | Instructions | Types of | Defaults |
| :--- | :--- | :--- | :--- |
| AllowClear | When this attribute is added, it supports clearing, and the radio mode is valid. | attribute | - |
| PlaceHolder | Select box default text | String | no |

## Options API

| parameter | Instructions | Types of | Defaults |
| :--- | :--- | :--- | :--- |
| Label | Display option content for display | String |  |
| \#OptionTemplate | Used to customize the display of the drop-down section option | of-template |  |
| Disabled | Is it disabled | Boolean | false |

