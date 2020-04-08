# Quill Editor

We have added the support for the famous Quill editor for Pages angular. Please refer there documentation here [https://github.com/KillerCodeMonkey/ngx-quill](https://github.com/KillerCodeMonkey/ngx-quill)

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { QuillModule } from 'ngx-quill'
@NgModule({
  imports: [QuillModule,...]
})
export class AppModule(){}
```

## How to use 

Basic Select with Search

{% tabs %}
{% tab title="HTML" %}
```markup
<quill-editor [style]="{height: '350px'}" placeholder="" ></quill-editor>
```
{% endtab %}
{% endtabs %}



