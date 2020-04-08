# Layouts

Layouts in Pages help you to customize the main view of your app, this comes with pre built layout options that will be updated over time. Pages now comes with 5 Different layouts and each layout will have 7 themes.

Location : @pages/layouts  
  
All Layouts are extended from the super class rootLayout which is located in `@pages/layouts/root`

## Root Layout

### API <a id="api"></a>

| Property | Description | Type | Default | Scope |
| :--- | :--- | :--- | :--- | :--- |
| contentClass | Set content div class | string | null | Public |
| pageWrapperClass | Set Page Wrapper Class | string | null | Public |
| footer | Show / Hide Footer | boolean | true | Public |

### Functions

These functions can be called in any sub class layout.

```text
changeLayout(type:string);
```

Set body class layout. eg : - "menu-pinned'   


```text
openQuickView()
```

Open Quick view  


```text
openSearch()
```

Open Quick Search  


```text
toggleMenuPin($e)
```

Quick function to toggle fixed sidebar menu  


```text
toggleMenuDrawer()
```

Menu drawer in side bar. This function will close and open it.  


```text
toggleMobileSidebar()
```

Open and Close sidebar menu on mobile only  


```text
toggleSecondarySideBar()
```

Open and Close secondary sidebar on mobile only  


```text
toggleHorizontalMenuMobile()
```

Open and Close Sidebar on mobile - Implemented for Horizontal app menu  
  


## Sub Layouts

Layouts that are implemented extending root layout

### **condensed**

One of our most popular Layouts, Pages Condensed offers a wide range of responsive space specifically for dashboards with heavy content.   
  
Location -`@pages/layouts/condensed`  
  
  


### **casual**

A new tone of voice – a relaxed, friendly, joyful layout that quickly makes the user experience more personal, casual and fun!. Comes with horizontal layout and sidebar option   
  
Location -`@pages/layouts/casual`  
  
  


### **corporate**

Corporate is a bold, cool Layout that elevates your content by utilizing a clean layout and a simple, open interface. Contains boxed version and secondary sidebar.   
  
Location -`@pages/layouts/corporate`  
  
  


### **simplywhite**

In a world of complexity, Simplicity defeats stress. Simply white is an open simple, minimal yet striking layout, built to combat stress. Contains boxed version and secondary sidebar.   
  
Location -`@pages/layouts/simplywhite`  
  
  


### **executive**

A Professional template with a timeless look, best suited to quickly create a serious organized experience. Comes with horizontal layout and sidebar option   
  
Location -`@pages/layouts/executive`  


## Where are the styles imported?

Styles are imported for each layout SASS file. For example executive styles are imported from `@pages/layouts/executive/executive.component.scss`

{% hint style="info" %}
Note all components are styles are imported directly. You may wish to include what you use or import it directly to the component you use
{% endhint %}

