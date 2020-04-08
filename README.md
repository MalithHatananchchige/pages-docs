# Getting Started

## Introduction

Pages is carefully well thought UI frame work that is built on top of Bootstrap 4 and Angular 8+, Its hand crafted components look great on all devices and works super fast even on mobile. Pages ships with builtin native angular components -

* Cards
* Sliders
* Progress bars
* Notifications
* Date picker
* Time picker
* Drag and Drop Upload
* Select / Multi dropdown
* Switch Toggle
* List View
* Parallax
* Tag Input
* Retina 
* Siderbar
* Quickview
* Views

and many more. We have included popular angular components by thirdparty authors like   
ngx-bootstrap, ngnx-datatable and echarts.

## Getting Started

Use our `getting_started/angular` project to bootstrap your new idea. All demo content are stripped down . You can follow this documentation guide to include a other various components. But you can also refer up the demo source located in `demo/angular/` 

First follow angular [documentation](https://cli.angular.io/) on building and deploying

To run development server, navigate to demo/angular folder and run the command on your command line

```bash
ng serve
```

To deploy your app for production, navigate to demo/angular folder and run the command on your command line

```text
ng build --prod
```

Once your server is up and running navigate to the following URLs 

* [http://localhost:4200/condensed/](http://localhost:4200/condensed/)
* [http://localhost:4200/corporate/](http://localhost:4200/corporate/)
* [http://localhost:4200/simplywhite/](http://localhost:4200/condensed/)
* [http://localhost:4200/executive/](http://localhost:4200/simplywhite/)
* [http://localhost:4200/casual/](http://localhost:4200/casual/)

## Common Issues

### Error in rxjs module

`ERROR in node_modules/rxjs/internal/types.d.ts(81,44): error TS1005: ';' expected.`

* Remove the “node\_modules” folder from your project
* Go to package.json
* Change rxjs version to “rxjs”: “6.3.3”
* Go to console and run “npm install” again
* And then run “ng serve

### Invalid or unexpected token

After running ng serve command you get this error  
Invalid or unexpected token

* Delete package-lock.json
* Go to console and run “npm install” again
* And then run “ng serve



