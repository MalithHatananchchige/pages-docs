# Tree View

Tree view plugin is powered by a third party plugin. Please refer there documentation for further celebrations. [https://angular2-tree.readme.io/docs](https://angular2-tree.readme.io/docs)

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { TreeModule } from 'angular-tree-component';
@NgModule({
  imports: [TreeModule,...]
})
export class AppModule(){}
```

## How to use 

Basic Select with Search

{% tabs %}
{% tab title="HTML" %}
```markup
<tree-root [nodes]="simpleNodes" [options]="options" class="tree-wrapper bold-node-text level1-document-icon-only m-b-20"></tree-root>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
simpleNodes = [
    {
        id: 1,
        name: 'item1 with key and tooltip'
    },
    {
        id: 2,
        name: 'item2'
    },
    {
        id: 3,
        name: 'Folder with some children',
        children: [
        { id: 4, name: 'Sub-item 3.1',
            children:[
            {id: 5, name: 'Sub-item 3.1.1'},
            {id: 6, name: 'Sub-item 3.1.2'}
            ]
        },
        { id: 7, name: 'Sub-item 3.2',
            children:[
            {id: 8, name: 'Sub-item 3.2.1'},
            {id: 9, name: 'Sub-item 3.2.2'}
            ]
        }
        ]
    },
    {
        id: 10,
        name: 'Document with some children (expanded on init)',
        isExpanded:true,
        children: [
        { id: 11, name: 'Sub-item 4.1  (active and focus on init)',
        isFocused:true
        }
        ]
    },
];

options = {
    animateExpand:true,
};
```
{% endtab %}
{% endtabs %}

