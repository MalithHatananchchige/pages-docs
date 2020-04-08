# Typeahead

Typeahead is powered by the plugin ngx-bootstrap. Please refer there documentation for further details and instructions here [https://valor-software.com/ngx-bootstrap/\#/typeahead](https://valor-software.com/ngx-bootstrap/#/typeahead)

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { TypeaheadModule } from 'ngx-bootstrap';
@NgModule({
  imports: [TypeaheadModule,...]
})
export class AppModule(){}
```

## How to use 

{% tabs %}
{% tab title="HTML" %}
```markup
<div class="form-group typehead">
    <input placeholder="States of USA" [(ngModel)]="selectedState" [typeahead]="states"  [typeaheadScrollable]="true" [typeaheadOptionsInScrollableView]="5" class="form-control">
</div>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
  selectedState;
  states: string[] = [
    'Alabama',
    'Alaska',
    'Arizona',
    'Arkansas',
    'California',
    'Colorado',
    'Connecticut',
    'Delaware',
    'Florida',
    'Georgia',
    'Hawaii',
    'Idaho',
    'Illinois',
    'Indiana',
    'Iowa',
    'Kansas',
    'Kentucky',
    'Louisiana',
    'Maine',
    'Maryland',
    'Massachusetts',
    'Michigan',
    'Minnesota',
    'Mississippi',
    'Missouri',
    'Montana',
    'Nebraska',
    'Nevada',
    'New Hampshire',
    'New Jersey',
    'New Mexico',
    'New York',
    'North Dakota',
    'North Carolina',
    'Ohio',
    'Oklahoma',
    'Oregon',
    'Pennsylvania',
    'Rhode Island',
    'South Carolina',
    'South Dakota',
    'Tennessee',
    'Texas',
    'Utah',
    'Vermont',
    'Virginia',
    'Washington',
    'West Virginia',
    'Wisconsin',
    'Wyoming'
  ];
```
{% endtab %}
{% endtabs %}



