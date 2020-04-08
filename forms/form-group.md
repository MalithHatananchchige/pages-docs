---
description: Pages default form group directive.
---

# Form Group

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { SharedModule } from './@pages/components/shared.module';
@NgModule({
  imports: [SharedModule,...]
})
export class AppModule(){}
```

## Usage

Place "pgFormGroupDefault" in bootstrap forum-group div

![](../.gitbook/assets/screen-shot-2018-06-05-at-10.48.20-pm.png)

{% tabs %}
{% tab title="HTML" %}
```markup
<div class="form-group form-group-default required " pgFormGroupDefault>
    <label>Project</label>
    <input type="email" class="form-control" required >
</div>
```
{% endtab %}
{% endtabs %}



