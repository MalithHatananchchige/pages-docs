# Styles

Pages Angular is build using SCSS and you can find it in src/app/@pages/styles. This folder contains all modules with vendor / 3rd party plugin styles.

{% hint style="warning" %}
Its important to notice that each demo page / layout will have different modules included on runtime.
{% endhint %}

## How each page / layout has its own styles included 

Pages depend on layouts which are found in src/app/@pages/layouts. Layouts differ from the each route you have set in your main `src/app/app.routing.ts`    

example login and other session pages will not have most of the style modules included in other pages like progress bar & charts

```text
{
    path: 'condensed',
    component: BlankComponent,
    children: [{
      path: 'session',
      loadChildren: './session/session.module#SessionModule'
    }]
  },
```

the layout used in this is called "BlankComponent" if you visit @pages/layout/blank/blank.component.scss imported from styles folder.

Likewise each layout will have its own .scss file having its own module.

