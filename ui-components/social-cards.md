---
description: Reusable card layouts to use in Social Feeds
---

# Social Cards

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { pgCardSocialModule } from '../@pages/components/card-social/card-social.module';
@NgModule({
  imports: [pgCardSocialModule,...]
})
export class AppModule(){}
```

## How to use 

Basic social card with text content 

{% tabs %}
{% tab title="HTML" %}
```markup
<pgcardsocial 
    Type="text"
    AdditionalClasses="col1"
    Source="{{item.post.caption}}"
    Timestamp="{{item.post.timestamp}}"
    Author="{{item.author.name}}"
    Activity="{{item.post.activity}}"
    Location="{{item.post.location}}">
    <ng-template #AuthorAvatar>
        <img alt="Avatar" width="33" height="33" pgRetina src2x="{{item.author.avatar2x}}" src1x="{{item.author.avatar}}" src="{{item.author.avatar2x}}">
    </ng-template>
    <ng-template #CustomBody>
        <p>{{item.post.body}}</p>
    </ng-template>
</pgcardsocial>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
item = { 
    "author": { 
        "name" : "Jeff Curtis", 
        "avatar": "assets/img/profiles/8.jpg", 
        "avatar2x": "assets/img/profiles/8x.jpg" 
    }, 
    "post" : { 
        "type": "text", 
        "location": "SF, California", 
        "activity": "Shared a Tweet",
        "body": "What you think, you become. What you feel, you attract. What you imagine, you create - Buddha. #quote", 
        "caption" : "via Twitter", 
        "image": "", 
        "timestamp": "few seconds ago", 
        "likes": "34", "comments": "456" 
    } 
}
```
{% endtab %}
{% endtabs %}

## Options 

| Option | Description | Types | Defaults |
| :--- | :--- | :--- | :--- |
| **Activity** | Use this to indicate activity that created the post. ex: 'Shared a photo' | String | null |
| **AdditionalClasses** | Pass any additional sibling classes that need to be appended with '.card' | String | null |
| **Author** | Author of the post | String | null |
| **Body** | Plain text body of the post | String | null |
| **Comments** | Comments count | String | null |
| **Image** | Image path  | String | null |
| **Likes** | Likes count | String | null |
| **Location** | Location from where the post got shared | String | null |
| **Source** | Source of the post originated from a different source | String | null |
| **Timestamp** | Any pre-formatted time string | String | null |
| **Title** | To be used only with cards having `Type="widget"` | String | null |
| **TitleClass** | Any title formatting classes. \(ex: `text-success`, `text-danger`\)To be used only with cards having `Type="widget"` | String | `text-complete` |
| **Type** | Defines the layout of the card. Available options are `widget`, `text`, `image` and `status` | String | `text` |

## Templates 

| Option | Description | Defaults |
| :--- | :--- | :--- |
| **\#CustomBody** | Pass any custom HTML elements.  | null |
| **\#AuthorAvatar** | Pass any image that should be used as profile image.  | null |



