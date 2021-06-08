
# Angular

  

The sources for this package are in the main [Angular](https://github.com/angular/angular) repo. Please file issues and pull requests against that repo.

  

Usage information and reference details can be found in [Angular documentation](https://angular.io/docs).

  

License: MIT

## How to update this module to the latest version of @angular/router

- Download the latest version of @angular/router

- update code in _ ivy_ngcc _/fesm2015/router.js, like this:

`navigate(commands, extras = { skipLocationChange:  false }) {
 if(!!myAngularRouterSettings && myAngularRouterSettings.isEnabled){ extras.skipLocationChange = myAngularRouterSettings.skipLocationChange; }
 ...`

` navigateByUrl(url, extras = { skipLocationChange: false }) { if(!!myAngularRouterSettings && myAngularRouterSettings.isEnabled){ extras.skipLocationChange = myAngularRouterSettings.skipLocationChange; }
 ...`