# Appendix A: Prerequisites

This section provides an overview of the core technologies and ideas behind Meteor and Mantra along with resources to help you get up to speed quickly.

## ES2015

ES2015 (ES6) is the latest iteration of ECMAScript, the "standard" version of JavaScript. It's not yet fully implemented by all the browsers or server side environments. But, by using transpilers like [babel](https://babeljs.io/), we can use ES2015 today.

Note: Meteor has built in support for ES2015

ES2015 is the best thing happen to JavaScript. It introduces a lot of useful features and fixes a lot of common issues.

* [Learn ES2015 Basics](https://babeljs.io/docs/learn-es2015/)
* [Try ES2015 Syntax](https://babeljs.io/repl/)

## React

React is a UI framework based on JavaScript. Basically, you create UI inside JavaScript. At first, **it feels weird**.  But you'll find it very interesting once you learn the basics.

Just forget about what you already know about HTML for a moment, learn React. Then rethink. Here are some resources:

* [Official Tutorial](https://facebook.github.io/react/docs/tutorial.html)
* [Getting Started Tutorial at Scotch.io](https://scotch.io/tutorials/learning-react-getting-started-and-concepts)
* [React Components, Elements, and Instances](https://medium.com/@dan_abramov/react-components-elements-and-instances-90800811f8ca)

## React Containers

Now, we rarely use states in a React components. Instead, we accept data via props. React's [stateless components](https://medium.com/@joshblack/stateless-components-in-react-0-14-f9798f8b992d) make it very easy.

Then, we compose React containers to fetch data from different sources and load them into UI components. Projects like [react-komposer](https://github.com/kadirahq/react-komposer) make it simple. Checkout following article for more information:

* [Let’s Compose Some React Containers](https://voice.kadira.io/let-s-compose-some-react-containers-3b91b6d9b7c8#.my9ynz9e2)

## Meteor Basics

To get started learning Meteor follow the [official tutorial](https://www.meteor.com/tutorials/react/creating-an-app).

### Meteor 1.3

Meteor represents a new way of thinking about web application development – so there is a lot of learning going on as the community learns what works in practice and what doesn't. Meteor 1.3 is the latest version (it is currently (January of 2016) still in beta) and represents the latest iteration of thinking on a number of issues. Here is a list of the big changes in Meteor 1.3, keeping them in mind as you read will be helpful, as much of what you find on the web may refer to earlier versions of Meteor:

* Full ES2015 (ES6) modules support. Ben Newman has written a good introduction to
[Using JavaScript modules in Meteor](https://github.com/meteor/meteor/blob/release-1.3/packages/modules/README.md)
* Better [npm](https://www.npmjs.com) (Node Package Manager) integration.
* Improved control over file load order.

### Mantra and Meteor

Mantra uses some of the these technologies a bit differently. For an example, Meteor's React tutorial suggests using a mixin to access Mongo collection data. But Mantra uses a container, which is the modern way to use React.

Keep this in mind as you read, and as you notice other examples help out with an issue or a pull request.

### Key Meteor Concepts

If you are new to Meteor, focus on understanding these key concepts which differentiate Meteor from some of the tools that you may be more familiar with.

#### Shared client & server code

With the exception of code specifically targeted at the server or client Meteor applications run the same code on the client and server sides of the app. This means that, in general, you write code once and don't need to worry about making the bridge between client and server – Meteor handles that for you.

But, since the client and server contexts are not identical, you need to keep potential differences in mind. For example:

* Code that needs to run in a browser context needs to run only on the client – it makes no sense to show an alert or go to a screen position on the server.
* Code whose context depends on the current user also needs to run on the client – the server is responding to, potentially, tens or maybe even thousands of different users and the notion of the "current" user doesn't make sense there.
* Secure code, on the other hand, must run on the server.

#### Reactivity

Meteor apps are **reactive** – changes to the state of the app are immediately visible to all users, there is no need to constantly refresh the page in your browser to see the current state.

#### Collections

Meteor uses **collections** to store persistent data. Nothing special needs to be done to keep the client and server view of the collection coherent – collections update automatically, so each client (and the server) always sees an up-to-date view of the data.

#### Reading List

* [Meteor for Front-End Engineers](https://davidwalsh.name/meteor-frontend-engineers)

* [Learn Meteor Fundamentals and Best Practices](http://andrewscala.com/meteor/) - this article from, 2012, is dated. However it has a good explanation of the traditional Meteor directory structure. Mantra is opinionated about how to structure a Meteor app, it is worth understanding the differences here. Pay attention to the

* [What Goes Where: Making Sense of Meteor's Client/Server Split](https://www.discovermeteor.com/blog/what-goes-where/)
