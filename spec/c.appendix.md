# C. Appendix: Organizing Modules

Mantra has a 100% [module-based](#sec-Mantra-Modules) app architecture. There should be at least a single module.

We've discussed how to organize files inside a module and how to use them. But, we didn't discuss how to organize modules.

That's because it's different from app to app.

However, we are suggesting some potential patterns that can be used to organize modules.

## Single Core Module

For a simple app, we can put all the code inside a single module and name it as `core`. This would work for a simple app where there is a smaller client-side codebase.

## Core Module & Multiple Feature Modules

This is an extended version of the above "Single Module App" pattern. Here it is:

* We have a core module containing all the core client-side code, including all the routes in the app.
* Then we have different modules for major features in our app. These modules do not contain routes.

## Multi Modules

This the multi-module approach where there is no single core module.

* There are multiple modules for each main feature in the app.
* Each of them has its own route.

## Pages Module

NOTE: This can be used with any other pattern mentioned above.

Sometimes, we need to show some UI pages. They don't have their own actions, routes, or configurations. They only contain some UI code. These can be either UI components or some containers.

For this purpose, we can use an [implicit module](#sec-Implicit-Modules).
