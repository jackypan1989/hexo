---
title: These days I used AngularJS
date: 2015-11-03
tags:
- React
- Angular
- Javascript
categories:
- 程式設計
- Javascript
- React
---

There are so many leading front-end libraries such as [ReactJS](https://facebook.github.io/react/), [CycleJS](http://cycle.js.org/), [Elm](http://elm-lang.org/) …, etc. But, today I want to talk about [AngularJS](https://angularjs.org/), the first MV* framework I met.

<!-- more -->

![](https://medium2.global.ssl.fastly.net/max/2400/1*W1lQdBP_BKy8jz8jtW054w.jpeg)**

It’s been over two years since I started my full-stack development career. There are so that many interesting and error-trying stories could be shared. The first project we wrote was based on jQuery and Node.js, we soon encountered problems because of numerous sporadical unstructured javascript codes in our project.

So, we started to convert whole codebase into AngularJS framework. That’s exactly today’s topic I want to say. I was really amazed by the first look of demo on its official website. Especially, “**two-way data binding**”, you could easily bind the model to your view. The view automatically updated once model changed. How fantastic!

We used [MEAN](http://mean.io/#!/) stack (combination of MongoDB, Express, Angular, and Node.js) to be our starting point. Everything was great, the views of application were indeed developed so quickly. However, one year later, along with project’s growth, it became so hard to maintain whole application state and its performance. I started to consider about some techniques about virtual-dom and Flux … And rethink some core issues of AngularJS.

### It’s not simple. It tries to cover everything.

AngularJS want to do everything, you have to know so many concepts like module, controller, service, filter, routing, scope, directives …, etc. BANG! That’s why the guide book [ng-book](https://www.ng-book.com/) is up to 600+ pages. It’s hard to learn and cooperate for beginners.

### Not welcome for other libraries

If we want to use other libraries, we have to package them into AngularJS’ module. Although there are a bounty of contributors in community, it still would be a barrier for existing projects and WIP projects.

### HTML sugar somehow is not good.

We can view AngularJS as a strong jQuery because of its syntax sugar. After page loading, the core module will scan all DOMs with ng-syntax like ng-click, and bind the event on it. Nowadays, we all knew the manipulation of DOM is expensive. That’s why “html-based” AngularJS is not good for performance. And virtual-dom techniques will save us.

### **Two-way data binding, oh no.**

In the blackbox, the only thing we know is AngularJS will do all the model checks which we called ‘dirty check’. So we have to write more and more $watch and $observe to make sure the application state. Also, the $scope’s inheritance always breaks application data flow. After using Flux or other unidirectional data flow diagram, it’s much more easy to debug. WHAT?! Do you remember the amazing part we mentioned? Yes, we removed it. The core, “ng-model” is gone.

Hmmmmm… It sounds not cool for AngularJS lovers.

### Conclusion

Therefore, I started using [angular-virtual-dom](https://github.com/teropa/angular-virtual-dom) and [flux-angular](https://github.com/christianalfoni/flux-angular) to reconstruct whole program. Somehow, it’s already far away from original code and the application paradigm. That’s why we use [ReactJS](https://facebook.github.io/react/) with Flux-like data flow now, not AngularJS.

If you really want to use AngularJS, I strongly recommend it only in simple CURD cases. Or you may try the wholly different library [AngularJS 2.0](https://angular.io/).
