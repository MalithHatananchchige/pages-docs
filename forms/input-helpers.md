# Input Helpers

Input helpers are powered by the plugin Text Mask. Please refer there documentation for further details and instructions here [https://github.com/text-mask/text-mask](https://github.com/text-mask/text-mask)

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { TextMaskModule } from 'angular2-text-mask';
@NgModule({
  imports: [TextMaskModule,...]
})
export class AppModule(){}
```

## How to use 

{% tabs %}
{% tab title="HTML" %}
```markup
<div class="row">
    <div class="col-lg-6">
    <h5>
    Input masks
    </h5>
    <p>These assure the user will never enter invalid phone no, email or anything that has a pattern even without validations</p>
    <br>
    <div class="form-group">
        <label>Date</label>
        <span class="help">e.g. "25/12/2013"</span>
        <input [textMask]="{mask: mask.date}" type="text" id="date" class="form-control" guide="true">
    </div>
    <div class="form-group">
        <label>Telephone</label>
        <span class="help">e.g. "(324) 234-3243"</span>
        <input [textMask]="{mask: mask.telephone}" type="text" id="phone" class="form-control">
    </div>
    <div class="form-group">
        <label>Custom</label>
        <span class="help">e.g. "23-4324324"</span>
        <input [textMask]="{mask: mask.custom}" type="text" id="tin" class="form-control">
    </div>
    <div class="form-group">
        <label>Social Security Number</label>
        <span class="help">e.g. "432-43-2432"</span>
        <input [textMask]="{mask: mask.ssn}" type="text" id="ssn" class="form-control" placeholder="You can put anything here">
    </div>
    </div>
    <div class="col-lg-6">
    <h5>Input autonumeric
    </h5>
    <p>Do you forget small things? here is something that helps to automatically placed forgotten dollar signs, decimal places and even comma separates and many more!</p>
    <br>
    <div class="form-group">
        <label>Decimal place and comma separator</label>
        <span class="help">e.g. "53,000.00"</span>
        <input type="text" [textMask]="{mask: numberMask}" class="autonumeric form-control">
    </div>
    <div class="form-group">
        <label>Weird way but works</label>
        <span class="help">e.g. "45.000,00"</span>
        <input type="text" [textMask]="{mask: wierdMask}" class="autonumeric form-control">
    </div>
    <div class="form-group">
        <label>Dollar prefix</label>
        <span class="help">e.g. "$45.50"</span>
        <input type="text" [textMask]="{mask: dollarPrefix}" class="autonumeric form-control">
    </div>
    <div class="form-group">
        <label>Range</label>
        <span class="help">e.g. "0 - 9,999"</span>
        <input type="text" [textMask]="{mask: range}" class="autonumeric form-control">
    </div>
    </div>
</div>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
  //Input Examples Masks
  mask = {
    date : [/[1-9]/, /\d/,'/', /\d/, /\d/,'/', /\d/, /\d/, /\d/, /\d/],
    telephone:['(', /[1-9]/, /\d/, /\d/, ')', ' ', /\d/, /\d/, /\d/, '-', /\d/, /\d/, /\d/, /\d/],
    custom:[/[1-9]/, /\d/,'-', /\d/, /\d/, /\d/, /\d/, /\d/, /\d/, /\d/],
    ssn:[/[1-9]/, /\d/, /\d/,'-', /\d/, /\d/,'-', /\d/, /\d/, /\d/, /\d/],
  }
  numberMask = createNumberMask({
    prefix: '$ ',
    suffix: ''
  });
  wierdMask = createNumberMask({
    prefix: '',
    suffix: '',
    thousandsSeparatorSymbol:'.',
    allowDecimal:true,
    decimalSymbol:','
  });
  dollarPrefix = createNumberMask({
    prefix: '$ ',
    suffix: '',
    allowDecimal:true
  });
  range = createNumberMask({
    prefix: '',
    suffix: '',
    integerLimit:4
  });
```
{% endtab %}
{% endtabs %}



