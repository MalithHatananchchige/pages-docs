---
description: pg-menu-items
---

# Menu Items

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { SharedModule } from './@pages/components/shared.module';
@NgModule({
  imports: [SharedModule,...]
})
export class AppModule(){}
```

## How to use 

{% tabs %}
{% tab title="HTML" %}
```markup
<pg-menu-items [Items]="menuLinks">
</pg-menu-items>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
    menuLinks = [
      {
        label:"Dashboard",
        details:"12 New Updates",
        routerLink:"/",
        iconType:"pg",
        iconName:"home",
        thumbNailClass:"bg-success"
      },
      {
          label:"Email",
          details:"234 New Emails",
          routerLink:"email/list",
          iconType:"pg",
          iconName:"mail"
      },
      {
        label:"Social",
        routerLink:"social",
        iconType:"pg",
        iconName:"social"
      },
      {
          label:"Builder",
          routerLink:"builder",
          iconType:"pg",
          iconName:"layouts"
      },
      {
        label:"Layouts",
        iconType:"pg",
        iconName:"layouts2",
        toggle:"close",
        submenu:[
          {
            label:"Default",
            routerLink:"layouts/default",
            iconType:"letter",
            iconName:"dl",
          },
          {
            label:"Secondary",
            routerLink:"layouts/secondary",
            iconType:"letter",
            iconName:"sl",
          },
          {
            label:"Boxed",
            routerLink:"layouts/boxed",
            iconType:"letter",
            iconName:"bl",
          }
        ]
    },
      {
        label:"UI Elements",
        iconType:"letter",
        iconName:"Ui",
        toggle:"close",
        submenu:[
          {
            label:"Color",
            routerLink:"ui/buttons",
            iconType:"letter",
            iconName:"c",
          },
          {
            label:"Typography",
            routerLink:"ui/typography",
            iconType:"letter",
            iconName:"t",
          },
          {
            label:"Icons",
            routerLink:"ui/icons",
            iconType:"letter",
            iconName:"i",
          },
          {
            label:"Buttons",
            routerLink:"ui/buttons",
            iconType:"letter",
            iconName:"b",
          },
          {
            label:"Notifications",
            routerLink:"ui/notifications",
            iconType:"letter",
            iconName:"n",
          },
          {
            label:"Progress & Activity",
            routerLink:"ui/progress",
            iconType:"letter",
            iconName:"pa",
          },
          {
            label:"Tabs & Accordians",
            routerLink:"ui/tabs",
            iconType:"letter",
            iconName:"a",
          },
          {
            label:"Sliders",
            routerLink:"ui/sliders",
            iconType:"letter",
            iconName:"s",
          },
          {
            label:"Treeview",
            routerLink:"ui/tree",
            iconType:"letter",
            iconName:"tv",
          }
        ]
      },
      {
          label:"Forms",
          iconType:"pg",
          iconName:"form",
          toggle:"close",
          submenu:[
            {
              label:"Form Elements",
              routerLink:"forms/elements",
              iconType:"letter",
              iconName:"fe",
            },
            {
              label:"Form Layouts",
              routerLink:"forms/layouts",
              iconType:"letter",
              iconName:"fl",
            },
            {
              label:"Form Wizard",
              routerLink:"forms/wizard",
              iconType:"letter",
              iconName:"fq",
            }
          ]
      },
      {
          label:"Cards",
          routerLink:"cards",
          iconType:"pg",
          iconName:"grid"
      },
      {
          label:"Views",
          routerLink:"views",
          iconType:"pg",
          iconName:"ui"
      },
      {
          label:"Tables",
          iconType:"pg",
          iconName:"tables",
          toggle:"close",
          submenu:[
            {
              label:"Basic Tables",
              routerLink:"tables/basic",
              iconType:"letter",
              iconName:"bt",
            },
            {
              label:"Advance Tables",
              routerLink:"tables/advance",
              iconType:"letter",
              iconName:"dt",
            }
          ]
      },
      {
          label:"Maps",
          iconType:"pg",
          iconName:"map",
          toggle:"close",
          submenu:[
            {
              label:"Google Maps",
              routerLink:"tables/basic",
              iconType:"letter",
              iconName:"gm",
            },
            {
              label:"Vector Maps",
              routerLink:"tables/data",
              iconType:"letter",
              iconName:"vm",
            }
          ]
      },
      {
          label:"Charts",
          routerLink:"charts",
          iconType:"pg",
          iconName:"charts"
      },
      {
          label:"Extra",
          iconType:"pg",
          iconName:"bag",
          toggle:"close",
          submenu:[
            {
              label:"Invoice",
              routerLink:"extra/invoice",
              iconType:"letter",
              iconName:"in",
            },
            {
              label:"404 Page",
              routerLink:"tables/data",
              iconType:"letter",
              iconName:"pg",
            },
            {
              label:"500 Page",
              routerLink:"tables/data",
              iconType:"letter",
              iconName:"pg",
            },
            {
              label:"Login",
              routerLink:"session/login",
              iconType:"letter",
              iconName:"l",
            },
            {
              label:"Register",
              routerLink:"session/register",
              iconType:"letter",
              iconName:"re",
            },
            {
              label:"Lockscreen",
              routerLink:"session/lock",
              iconType:"letter",
              iconName:"ls",
            },
            {
              label:"Gallery",
              routerLink:"extra/gallery",
              iconType:"letter",
              iconName:"gl",
            },
            {
              label:"Timeline",
              routerLink:"extra/timeline",
              iconType:"letter",
              iconName:"t",
            }
          ]
      },
      {
        label:"Docs",
        routerLink:"http://pages.revox.io/dashboard/2.2.0/docs/",
        targe:"_blank",
        iconType:"pg",
        iconName:"note"
      },
      {
        label:"Changelog",
        externalLink:"http://changelog.pages.revox.io/",
        targe:"_blank",
        iconType:"letter",
        iconName:"Cl"
      },
  ];
```
{% endtab %}
{% endtabs %}

### Menu Items Structure

| Label | Description | Type | Example |
| :--- | :--- | :--- | :--- |
| label | Name of the menu item that appears | string | Dashboard |
| details | Sub Text that is shown below the label | string | 2 Unread |
| routerLink | Route link path | string | /ui/buttons |
| iconType | Icon type - Font awesome, Pages Icons, Feather & also supports Letter  | string | pg, fe, letter, material |
| iconName | The class name of the icon or abbreviation letters | string | pg-user |
| toggle | Sub menu close or open : "close", "open" | string | close / open |
| externalLink | Used for connecting to another URL | string  | http://example.com |
| target | Used with "externalLink" to open in a new window / tab | string | \_blank |
| submenu | Sub menu items  | array\[\]:string |  |

