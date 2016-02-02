# C. Appendix: Organizing Modules

Mantra has a 100% [module based](#sec-Mantra-Modules) app architecture. There should be at least a single module.

We've discussed about how to organize files inside a module and how to use them. But, we didn't discuss about how to organize modules.

That's because it's different from app to app.

However, now we are trying to suggest some potential patterns which can be used to organize modules.

## Single Core Module

For an simple app, we can put all the code inside a single module and name it as `core`. This would work for a simple app where there are a few client side code (or complexity).

## Core Module & Multiple Feature Modules

This is an extended version of the above "Single Module App" pattern. Here it is:

* We've a core module containing all the core client side code including all the routes in the app.
* Then we have separate modules for major features in our app. These modules do not contain routes.

## Multi Modules

This the multi module approach where there is no single core module.

* There are multiple modules for each main feature in the app.
* Each of them have their own routes.

## Pages Module

NOTE: This can be used with any other pattern mentioned above.

Sometimes, we need to show some UI pages. They don't have their own actions, routes or configurations. They only contain some UI code. These can be either UI components or some containers.

For this purpose, we can use an [implicit module](#sec-Implicit-Modules).
