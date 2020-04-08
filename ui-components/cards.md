---
description: Pages cards
---

# Cards

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { pgCardModule} from './@pages/components/card/card.module';
@NgModule({
  imports: [pgCardModule,...]
})
export class AppModule(){}
```

## How to use 

{% tabs %}
{% tab title="HTML" %}
```markup
<pgcard (onRefresh)="sampleRefresh()" [Loading]="isLoading" [ShowMessage]="errorMessage" [Message]="message">
    <ng-template #CardTitle>Sample</ng-template>
    <ng-template #CardExtraControls>                
    <li>
        <div class="dropdown" dropdown>
            <a href="javascript:void(0);" dropdownToggle role="button" aria-expanded="false">
            <i class="card-icon card-icon-settings "></i>
            </a>
            <div class="dropdown-menu dropdown-menu-right" *dropdownMenu  role="menu" aria-labelledby="card-settings">
            <a href="javascript:void(0);" class="dropdown-item">API</a>
            <a href="javascript:void(0);" class="dropdown-item">Preferences</a>
            <a href="javascript:void(0);" class="dropdown-item">About</a>
            </div>
        </div>
    </li>
    </ng-template>
    <h3>
    <span class="semi-bold">Advance</span> Tools</h3>
    <p>We have crafted Pages Cards to suit any use case. Add a maximize button <i class="pg-fullscreen"></i> into your Cards controls bar to make the Cards go full-screen. This will come handy if you want to show lot of content inside a Cards and want to give the content some room to breath</p>
    <br>
    <div>
        <div class="profile-img-wrapper m-t-5 inline">
        <img width="35" height="35" src2x="assets/img/profiles/avatar_small2x.jpg" pgRetina src1x="assets/img/profiles/avatar_small.jpg" alt="" src="assets/img/profiles/avatar_small2x.jpg">
        <div class="chat-status available">
        </div>
        </div>
        <div class="inline m-l-10">
        <p class="small hint-text m-t-5">VIA senior product manage
            <br>for UI/UX at REVOX</p>
        </div>
    </div>             
</pgcard>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
  constructor() { }

  ngOnInit() {
  }
  isLoading:boolean=false;
  errorMessage:boolean=false;
  message:string = "Something went terribly wrong. Just keep calm and carry on!";
  
  sampleRefresh(){
    this.isLoading = true;
    this.errorMessage = false;
    setTimeout(()=>{
          this.isLoading = false;
          this.errorMessage = true;
    },3000);
  }
```
{% endtab %}
{% endtabs %}

## API

| Property | Description | Type | Default |
| :--- | :--- | :--- | :--- |
| Loading | To show loading Progress Bar with overlay | boolean | false |
| ShowMessage | Show message once load is failed | boolean | false |
| Message | Error message you want to show | string | null |
| Maximize | Show Maximize button | boolean | true |
| Refresh | Show Refresh button | boolean | true |
| Toggle | Show Collapse toggle button | boolean | true |
| Maximize | Show maximize button | boolean | true |
| ProgressType | Type of progress bar - circle , bar | boolean | circle |
| ProgressColor | Color of the progress bar | string | success, danger, warning and primary |
| MinimalHeader | No controls. A simple circular refresh button | boolean | false |
| HeaderClass | Add extra header class to the card | string | null |
| Type | Class of card, transparent, default or with bg-color | string | default |

## Callbacks

| Method | Description |
| :--- | :--- |
| onRefresh\(\) | When Refresh button is triggered |

