---
description: Pages Progress bar / circular
---

# Progress Bar

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { ProgressModule } from '../@pages/components/progress/progress.module';
@NgModule({
  imports: [ProgressModule,...]
})
export class AppModule(){}
```

## Usage

{% tabs %}
{% tab title="HTML" %}
```markup
<pg-progress type="bar" color="primary" value="35" thick="true"></pg-progress>

<pg-progress type="bar" indeterminate="true" thick="true"></pg-progress>

<pg-progress type="circle" color="complete" value="75" ></pg-progress>

<pg-progress type="circle" value="75" thick="true"></pg-progress>
```
{% endtab %}
{% endtabs %}

## API

| parameter | Instructions | Types of | Defaults |
| :--- | :--- | :--- | :--- |
| type | Type of progress  | string | bar / circle |
| color | Bootstrap primary colors | string | primary, success, etc |
| value | Percentage of progress | integer | 0 |
| indeterminate | When progress value is unknown | boolean | false |
| thick | Will increase the thickness | boolean | true |

