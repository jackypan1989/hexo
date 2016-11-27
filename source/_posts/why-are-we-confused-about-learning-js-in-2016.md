---
title: Why are we confused about learning JS in 2016
date: 2016-10-06
tags:
- Javascript
- 2016
- React
- Webpack
categories:
- 程式設計
- Javascript
---

It's an article response to the article [How it feels to learn JavaScript in 2016](https://hackernoon.com/how-it-feels-to-learn-javascript-in-2016-d3a717dd577f)

Recently, we've heard too many terms in JS community in 2016. Why? So, let's talk about these.

<!-- more -->

# Core Code
## Who started the war? [Angular](AngularJS) 1.x
At first, it's just a small JS lib reinvented from jQuery to handle relationship among view, logic, and model. After that we found we don't need to write some shit and hard maintained codes in one single file with heavy logic. That's also what we called MVC or MVVM in front-end JS.

There is not only one to handle this problem, like backboneJS and emberJS. They all try to solve the potential problems when app getting bigger. But indeed Angular makes the front-end community hotter and started arguing the best practice.

## So, what and why [ReactJS](ReactJS)?
Basically, the view (HTML's DOM) manipulation also a big performance problem when adding many components onto you HTML. So, the Facebook released the ReactJS to handle the view rendering, it started using the concept of virtual-dom. The algorithm of virtual-dom increases the performance so much! So many libs also started to embrace virtual-dom.

Another side is Flux-like style. It differs from MVC/MVVM code base. It provides another way to think the model's flow and business logic. And it works great! It also helps you debug in a one-direction way and quickly find the bug.

## ReactJS is great. Why [ReduxJS](ReduxJS), [CycleJS](CycleJS) ... etc
Before talking about that, we know we learned so many OOP concepts (like JAVA, python, C# ... ) But the functional programming is getting more hotter (like Scala, Closure, Haskell ...) So these lib begins to ref some great ideas from FP language. Also, it helps us to build a more solid application.

Like CycleJS is virtual-dom with functional programming, and ReduxJS is a functional programming lib to handle ReactJS's model.

# Tools
## Why [BabelJS](BabelJS])?
Although the evolution of JS is not so much quick, the old browsers could still not handle the new syntax . BabelJS provide us to transform new edition JS (ES6, ES7+, and others) to old edition JS (with old IE blablabla).

## [Webpack](Webpack), Grunt, Gulp?
They are building tool, help you to manage the development flow. Maybe you want to compress your JS file, include some third-party library, create a good testing process, etc.

## NPM, bower ...?
Just like ANT, Maven(Java), Gem(Ruby), and PIP(Python). These manage your project's dependency.

# [TypeScript](TypeScript), ClosureScript ,PureScript, ELM ... ?
In the beginning, Javascript is just a tiny tool to handle html event, like click event and show a message. No one knows Javascript will dominate the web application world. Javascript still exists some unavoidable weakness and legacy issue. Like strong type annotation, it would give us good maintain experience and static analysis with IDE.
That's why these languages are coming up. And they all can compile to Javascript :p

# Conclusion
Don't be scared of these terms. They are not here for no reason, according to your requirement, you may need easy testing, good maintenance ... or just a simple page with jQuery and HTML.

It's no more than usual when community getting bigger.
It's just a signal showed that the Javascript is dominating the dev world.

[AngularJS]: https://angularjs.org/
[ReactJS]: https://facebook.github.io/react/
[BabelJS]: https://babeljs.io/
[Webpack]: https://webpack.github.io/
[TypeScript]: https://www.typescriptlang.org/
[CycleJS]: http://cycle.js.org/
[Redux]: https://github.com/reactjs/redux
[ELM]: http://elm-lang.org/
