---
description: pg-header
---

# Header

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { HeaderComponent } from './@pages/components/header/header.component';
@NgModule({
  declarations: [HeaderComponent,...]
})
export class AppModule(){}
```

## How to use 

{% tabs %}
{% tab title="HTML" %}
```markup
<pg-header [boxed]="_boxed">
<!-- YOUR HEADER CONTENT GOES HERE -->
</pg-header>
```
{% endtab %}
{% endtabs %}

## API

| Property | Description | Type | Default |
| :--- | :--- | :--- | :--- |
| boxed | Wraps content with a container div | boolean | false |



