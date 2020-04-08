# Parallax

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

Place "pg-parallax" in any div you want to get the parallax effect

{% tabs %}
{% tab title="HTML" %}
```markup
<div class="inner" pg-parallax>
</div>
```
{% endtab %}
{% endtabs %}



