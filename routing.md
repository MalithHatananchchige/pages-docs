# Routing

## **Basic Routing**

Routing is a key component is a must read if you want to get a clear understanding of how layouts change from each route. All sample routes are in `src/app/app.routing.ts`. You may wish to remove all routes and add your routes. First select the what your [root layout](untitled.md) you want it to be. Here I will use Condensed layout

```javascript
import { Routes } from '@angular/router';
//Layouts
import { 
  CondensedComponent,
  BlankComponent,
} from './@pages/layouts';

//Single Page
import { CondensedDashboardComponent} from './dashboard/condensed/dashboard.component';

export const AppRoutes: Routes = [
  {
    path: 'home',
    component: CondensedComponent,
    children: [{
      path: 'dashboard',
      //Sub Single Page
      component: CondensedDashboardComponent
    }],
  },
]
```

CondensedComponent is your condensed layout located in @pages/layouts/condensed it contains HTML and SCSS imports required for it to work with all UI / form components scss files as well. In the first route I have used

```javascript
  {
    path: 'home',
    component: CondensedComponent,
    children: [{
      path: 'dashboard',
      component: CondensedDashboardComponent
    }],
  },
```

`component: CondensedComponent` is where the root layout is assigned and inside the children is your sub pages. So I have imported a sample sub page and assigned it  


```javascript
{
      path: 'dashboard',
      component: CondensedDashboardComponent
}
```

Your routing path will `home/dashboard`

### 

### Nested Routing

Instead of routing to one single page you may want to route into a sub router making it a nested routing.

```javascript
  {
    path: 'home',
    component: CondensedComponent,
    children: [{
      path: 'ui',
      loadChildren: './ui/ui.module#UiModule'
    }]
  }
```

Instead of loading a single component you simply add loadChildren: './ui/ui.module\#UiModule' you need to make sure that ui.module or your sub module globally assigned / imported in the app.module.ts file for the router to understand.  
  
Next in your sub module folder make routing.ts file. In the example src/app/ui/ui.routing.ts

```javascript
import { Routes } from '@angular/router';

//Sample Demo pages
import { ButtonspageComponent } from './buttonspage/buttonspage.component';

export const uiRoute: Routes = [
    {
      path: 'buttons',
      component: ButtonspageComponent
    }
]
```

This will import all the sub pages in that folder with its path and component name as show in the sample code above.

Lastly make a submodule folder so your route component can import them all at once. This sub module folder will import any dependencies required in your sub pages.

```javascript
//Angular Dependencies
import { NgModule } from '@angular/core';
import { CommonModule } from '@angular/common';
import { RouterModule } from '@angular/router';
import { HttpModule} from '@angular/http';
import { HttpClientModule } from '@angular/common/http';
//Requires Forms to be imported for Checkbox buttons
import { FormsModule, ReactiveFormsModule } from '@angular/forms';

//This is your sub router
import { uiRoute } from './ui.routing';

@NgModule({
  imports: [
    CommonModule,
    SharedModule,
    HttpModule,
    HttpClientModule,
    RouterModule.forChild(uiRoute)
  ],
  declarations: [ButtonspageComponent],
  providers: []
})
export class UiModule { }
```

The above code is a sample module ts that has its own sub router `import { uiRoute } from './ui.routing';` and declarations of its own sub pages. Importing this to the main app router will help create nested routing 

### \*\*\*\*

### **Missing styles**

While your importing layouts to your main app.routing.ts. If a component has missing styles check @pages/layout/layout-name/layout-name.component.scss;

eg : @pages/layout/condensed/condensed.scss;

