---
description: pg-secondary-sidebar
---

# Secondary Sidebar

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { SharedModule } from './@pages/components/shared.module';
@NgModule({
  declarations : [SidebarComponent,...]
  imports: [SharedModule,...]
})
export class AppModule(){}
```

## Example

{% tabs %}
{% tab title="HTML" %}
{% code title="" %}
```markup
<pg-secondary-sidebar>
<!-- YOUR CONTENT GOES HERE -->
</pg-secondary-sidebar>
```
{% endcode %}
{% endtab %}
{% endtabs %}

