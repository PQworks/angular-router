
# Angular

  

The sources for this package are in the main [Angular](https://github.com/angular/angular) repo. Please file issues and pull requests against that repo.

  

Usage information and reference details can be found in [Angular documentation](https://angular.io/docs).

  

License: MIT

## How to update this module to the latest version of @angular/router

- Download the latest version of @angular/router

- update code in each */router.mjs file (you can use VSCode global search for navigateByUrl) , like this:

```
 navigateByUrl(url, extras = {
        skipLocationChange: false
    }) {
        if(!!myAngularRouterSettings && myAngularRouterSettings.isEnabled){ 
            extras.skipLocationChange = myAngularRouterSettings.skipLocationChange; 
            extras.replaceUrl = myAngularRouterSettings.replaceUrl;
        }
        ...
    }
 ```

```
    navigate(commands, extras = { skipLocationChange: false }) {
        if(!!myAngularRouterSettings && myAngularRouterSettings.isEnabled){ 
            extras.skipLocationChange = myAngularRouterSettings.skipLocationChange; 
            extras.replaceUrl = myAngularRouterSettings.replaceUrl;
        }
        ...
    }
 ```

 - Replace all files with the new ones (keep README file only)
 - Remove "_integrity" field from the new package.json
 - Publish your changes 🎉
