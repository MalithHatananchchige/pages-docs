# Notifications

Pages Notification service that can be invoked from any page or component

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { MessageModule } from '../@pages/components/message/message.module';
import { MessageService } from '../@pages/components/message/message.service';
@NgModule({
  imports: [MessageModule,...],
  providers: [MessageService,...]
})
export class AppModule(){}
```

## How to use 

{% tabs %}
{% tab title="Typescript" %}
```typescript
import { Component, OnInit } from '@angular/core';
import { MessageService } from '../../@pages/components/message/message.service';

@Component({
  selector: 'app-notificationspage',
  templateUrl: './notificationspage.component.html',
  styleUrls: ['./notificationspage.component.scss'],
})
export class mySamplePage implements OnInit {

  constructor(private _notification: MessageService) { 
  }

  ngAfterViewInit() {
      this._notification.create(
          "primary",
          "Hello World",
          {
          Position:"top",
          Style:"bar",
          Duration:0
          }
      );
  }

}

```
{% endtab %}
{% endtabs %}

## API

**Global configuration \(Config\)**

| parameter | Types of | Defaults | Instructions |
| :--- | :--- | :--- | :--- |
| Duration | Number | 0 | Duration, does not disappear when set to 0  |
| Position | String | top |  also supports bottom \| bottom-left \| bottom-right \| top-left \| top-right |
| Style | String | bar | bar  \| circle \| simple |
| MaxStack | Number | 8 | The maximum number of prompts that can be displayed |
| PauseOnHover | Boolean | true | Pause countdown when mouse is over |

  
**MessageService service**

| method | parameter | Instructions |
| :--- | :--- | :--- |
| create | `(type: string, content: string, options?: Object)` | Provide type attribute, can be passed in options such as 'success' |
| html | `(html: string, options?: Object)` | HTML content can be used to render content |
| remove | `(id?: string)` | Remove specific id message, remove all messages when id is empty |

