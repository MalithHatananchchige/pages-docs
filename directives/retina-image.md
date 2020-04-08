---
description: Load Retina Images from img tag
---

# Retina Image

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

Place "pgRetina" in any image / img tag

{% tabs %}
{% tab title="HTML" %}
```markup
<img src="assets/img/profiles/avatar.jpg" alt="" pgRetina src1x="assets/img/profiles/avatar.jpg" src2x="assets/img/profiles/avatar_small2x.jpg" width="32" height="32">
```
{% endtab %}
{% endtabs %}

## API

| parameter | Instructions | Types of | Defaults |
| :--- | :--- | :--- | :--- |
| src1x | Load original image path | string | null |
| src2x | Load Retina image path | string | null |

