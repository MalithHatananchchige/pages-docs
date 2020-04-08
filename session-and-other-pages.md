---
description: 'Pages ship with a few session pages like login, register, & lock screen.'
---

# Session and other pages

Session pages are found under the module sessionModule which can be located in `src/app/session` folder. There is no[ root component / Layout](untitled.md) assigned from these components. Each page / session page [layout](untitled.md) is [assigned](untitled.md) from the router. 

{% tabs %}
{% tab title="Typescript" %}
{% code title="app.routing.ts" %}
```javascript
import { Routes } from '@angular/router';
//Layouts
import { 
  CondensedComponent,
  BlankComponent,
} from './@pages/layouts';

export const AppRoutes: Routes = [

  {
    path: '',
    //Your root layout
    component: BlankComponent,
    children: [{
      path: 'session',
      loadChildren: './session/session.module#SessionModule'
    }]
  }
];

```
{% endcode %}
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

In the sample router note that `BlankComponent` is imported from `@pages` - located in the folder @pages/layouts. And this import is used in the `component:BlankComponent` of the sample code above. Note that in BlankComponent we have only loaded styles relevantly needed for that module. You can see it in `@pages/layouts/blank/blank.component.scss`   


### Can we used the condensedLayout for sessionModules / Session Pages

Yes you can, make sure you have imported CondensedLayout from

`import { CondensedComponent} from './@pages/layouts';`

Then you need to make sure the styles are imported to your `@pages/layouts/condensed/condensed.component.scss`

**Styles that are required for Session Pages**

```css
//Login
@import "modules/login.scss";

//Lock screen
@import "modules/lock_screen.scss";

//Error
@import "modules/_error.scss";
```

_You can try this with any layout you like in @pages/layouts_

