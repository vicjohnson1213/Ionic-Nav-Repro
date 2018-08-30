# Ionic-Nav-Repro

> A reproduction of an Ionic bug where two pages exist on the page simultaneously.

## What's Wrong?

When navigating back and forth between two pages, both pages remain in the DOM if you try to navigate again before the first animation is finished. The top page is not visible, but it prevents you from interacting with the lower page that is visible.

## Ionic Info

```
Ionic:

   ionic (Ionic CLI)          : 4.1.1 (C:\Users\victor.johnson\AppData\Roaming\npm\node_modules\ionic)
   Ionic Framework            : @ionic/angular 4.0.0-beta.5
   @angular-devkit/core       : 0.7.5
   @angular-devkit/schematics : 0.7.5
   @angular/cli               : 6.1.5
   @ionic/ng-toolkit          : 1.0.7
   @ionic/schematics-angular  : 1.0.5

System:

   NodeJS : v8.11.2 (C:\Program Files\nodejs\node.exe)
   npm    : 5.6.0
   OS     : Windows 10
```

## Steps to Reproduce

1. Click on `GO TO THE SECOND PAGE`
2. Click on `GO BACK BY CLICKING HERE`
3. Quickly repeat steps 1 and 2.

## Expected behavior

The app should navigate back and forth between the two pages without leaving any residual pages in the DOM.
