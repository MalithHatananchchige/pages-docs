---
description: Pages List View
---

# List View

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { pgListViewModule} from './@pages/components/list-view/list-view.module';
@NgModule({
  imports: [pgListViewModule,...]
})
export class AppModule(){}
```

## How to use 

Basic Select with Search

{% tabs %}
{% tab title="HTML" %}
```markup
<pg-list-view-container class="scrollable full-height" [perfectScrollbar]="config">
    <pg-list-item *ngFor="let group of userList">
        <ng-template #ItemHeading>
            {{group.group}}
        </ng-template>
      <li class="chat-user-list clearfix"  *ngFor="let user of group.users">
        <a pg-view-trigger parentView="chat" animationType="push-parrallax">
            <span class="thumbnail-wrapper d32 circular bg-success">
                <img width="34" height="34" alt="" src="{{user.img}}" class="col-top">
            </span>
            <p class="p-l-10 ">
              <span class="text-master">{{user.username}}</span>
              <span class="block text-master hint-text fs-12">{{user.lastMessage}}</span>
            </p>
          </a>
        </li>
    </pg-list-item>
</pg-list-view-container>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
userList = [];
```
{% endtab %}
{% endtabs %}

## 

