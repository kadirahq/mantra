# Appendix A: Prerequisite

These resources will help you understand Mantra very clearly.

## ES2015

ES2015 is the standard version of JavaScript for 2015. It's not fully implemented by all the browers or server side enviroments. But, using transpilers like [babel](https://babeljs.io/), we could use E2015 today.

Note: Meteor has built in support for ES2015

ES2015 is the best thing happen to JavaScript. It introduce a lot of features and fixes a lot of common issues.

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

Then, we compose React containers to fetch data from different sources and load them into UI components. Projects like [react-komposer](https://github.com/kadirahq/react-komposer) make is simple. Checkout following article for more information:

* [Let’s Compose Some React Containers](https://voice.kadira.io/let-s-compose-some-react-containers-3b91b6d9b7c8#.my9ynz9e2)

## Meteor Basics

You need to have better understanding of Meteor. For that follow Meteor's [official tutorial](https://www.meteor.com/tutorials/react/creating-an-app).

Note: Mantra use some of the above technologies bit differently. For an example, Meteor's react tutorial suggest to use a mixin to access Meteor data. But Mantra uses a container, which is the modern way to use React.
