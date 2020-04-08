# Overlay Search

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
<pg-search-overlay></pg-search-overlay>
```
{% endcode %}
{% endtab %}
{% endtabs %}

## Location

This component is located in @pages/components/search-overlay

{% hint style="info" %}
It does not have an ngOutlet for adding content in. Use the search-overlay.component.html
{% endhint %}

## How to toggle

Include the Toggle service as mention here to any external component us wish

Then use the following function to open

```text
toggleSearch(true)
```

