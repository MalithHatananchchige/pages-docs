# Themes

This part of the documentation will explain how to change the current theme to pages pre-build themes, pages themes are made with concentrated color palete and its not just changing the theme to pure red but entire color pallet and its done by just replacing one line of code  


## **Using CSS**

We have already included 4 pre-made themes found inside `pages/css/themes/` To switch the theme remove the existing pages.css to the one located in inside `themes/` folder

1. Default

   ```markup
   <link class="main-stylesheet" href="pages/css/pages.css" rel="stylesheet" type="text/css" />
   ```

2. Corporate

   ```markup
   <link class="main-stylesheet" href="pages/css/themes/corporate.css" rel="stylesheet" type="text/css" />
   ```

3. Retro

   ```markup
   <link class="main-stylesheet" href="pages/css/themes/retro.css" rel="stylesheet" type="text/css" />
   ```

4. Unlax

   ```markup
   <link class="main-stylesheet" href="pages/css/themes/unlax.css" rel="stylesheet" type="text/css" />
   ```

5. Abstract

   ```markup
   <link class="main-stylesheet" href="pages/css/themes/abstract.css" rel="stylesheet" type="text/css" />
   ```

## **Using SCSS**

SCSS works much easier where you can switch the theme by simply changing the import path to the variable file.  
  
The import is located at `pages/scss/pages.scss` 

#### Default

```css
// Import Vars
@import "var";
```

#### Change to 

```css
// Import Vars
@import "themes/abstract/var";
```

you can change it to any the in the pages/scss/themes folder

## **Creating your own theme**

The themes will be found under `pages/scss/theme/` folder

**Step One**

Create a new folder under the `scss/theme/my_theme`

**Step Two**

Create a new file name called `theme.scss` under the `scss/theme/my_theme` and add the following code

```text
@import "var";
```

**Step Three**

Create a new file name called `var.scss` under the `scss/theme/my_theme` and import the code of`scss/theme/abstract/var.scss` to it and change the following variables   
  
**Main Base color** 

```css
$color-contrast-lowest: #fff; 
$color-contrast-higher: #121212;
```

#### Primary Color

```css
$color-primary: #6462e6;
$color-complete: #2979fb; 
$color-success: #00cea0; 
$color-warning: #fece40; 
$color-danger: #f13d5b; 
$color-info: #363c52; 
$color-menu: #3b3a48;
```

**Step Four**

Change the variable `$theme-name` to your theme name in `scss/pages.scss`

