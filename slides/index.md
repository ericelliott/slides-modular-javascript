> "Absorb what is useful, discard what is not, add what is uniquely your own."
~ Bruce Lee

---

# Modular JavaScript With npm and Node Modules

_Eric Elliott_

---

![adobe](adobe.jpeg)

![tout](https://raw.github.com/dilvie/fluent-prototypal-oo/master/tout.jpg)
 ![bandpage](https://raw.github.com/dilvie/fluent-prototypal-oo/master/bandpage.jpg)
 ![zumba](https://raw.github.com/dilvie/fluent-prototypal-oo/master/zumba.jpg)

---

![Programming JavaScript Applications](http://akamaicovers.oreilly.com/images/0636920033141/lrg.jpg)

---

# Why Modules?

---

## DRY (Don't Repeat Yourself)

---

## Stay Organized

---

## Maintain Separation of Concerns

---

## Domain logic

---

## Presentation

---

# Different Modules

---

# Why Node Style Modules?

---

## Stupid Simple Syntax

---

### Export Something

```js
'use strict'; // You should always do this.

var foo = function () {
  return true;
};

module.exports = foo;
```
---

### Import Something

```js
var foo = require('./foo.js');

foo(); // true
```

---

## Unbeatable ecosystem

![module-counts](module-counts.png)

---

## Great Package Management

---

## Keep all modules in Git

---

# Principles of Modularity

Modules should be:

---

## Specialized

DOT (Do One Thing)

---

## Independent

* Do something useful independent of the app.
* Don't grab stuff from globals.

---

## Decomposable

* You should be able to test your modules outside your app.
* Like component entertainment center.

---

## Recomposable

* Should be possible to rearrange the modules to build a different app.

---

## Substitutable

* You should be able to swap out one module for another, as long as they share the same public interface.

---

## Open / Closed

Open to extension, closed to modification

---

# Interfaces

> "Program to an interface, not an implementation."

~ GoF, "Design Patterns"

---

## Interface is a Contract

* Enables substitution

---

## Obey the Open / Closed Principle

---

## Export Your Public API

---

## Encapsulate Your Implementation

* Easy - just don't export it!

---

```js
// Not exported.
var fullName = function fullName(firstName, lastName) {
  return firstName + ' ' + lastName;
}

module.exports = function person(options) {
  instance.firstName = options.firstName;
  instance.lastName = options.lastName;

  // Hides internal implementation.
  instance.name = function name() {
    return fullName(this.firstName, this.lastName);
  }
};
```

---

## KISS (Keep It Simple, Stupid)

---

## Keep It Stupid Simple

---

> It’s not the daily increase but daily decrease.

> Hack away at the unessential.
~ Bruce Lee

---

## Export One Function
* Principle of high cohesion

---

### Lame:
```js
module.exports.foo = function () { return 'foo'; };
module.exports.bar = function () { return 'bar' };
module.exports.baz = function () { return 'baz'; };
```
---
```js
var foo = require('lame').foo,
  bar = require('lame').bar,
  baz = require('lame').baz;
```

---

### Better - different modules.
```js
var foo = require('foo'),
  bar = require('bar'),
  baz = require('baz');
```

---

### High cohesion warrants object factories:
```js
var http = require('http'),
  server = http.createServer();

server.listen(3000, function () {
  setTimeout(function () {

    server.close();

  }, 30000)
});
```

---

## Don't Export Constructors

---

## Breaks open / closed principle
```js
var Widget = require('widget'),
  myWidget = new Widget('clock');
```

---

## Can't turn widget into factory
* All callers are expecting to use `new`

---

## Do Export Factories
```js
var widget = require('widget'),
  myWidget = widget();
```

---

## Inside the widget factory:
```js
module.exports = function widget(options) {
  return {
    name: options.name,
    el: document.createElement(options.tagName || 'div'),
    template: '<div class="content"></div>'
  }
};
```

---

## Factory flexibility

Stampit: Compose factory functions.
```js
module.exports = function (options) {
  return stampit.compose(widget, eventEmitter,
    list, touch, intfiniteScroll);
};
```

---

# npm - not an acronym

Node Packaged Modules (60k+175/day)

---

## Bundled with Node

http://nodejs.org/download/

---

## Version using semver

major.minor.patch

---

* major = breaking changes
* minor = new non-breaking features
* patch = bug fixes, insignificant changes

---

## package.json

* name
* version
* author
* description
* keywords
* repository
* license

---

## more package.json

* main
* scripts
* dependencies, bundledDependencies
* devDependencies
* private

---

## Public and private dependencies:
```
"dependencies": {
    "public": "git://github.com/user/repo.git#ref"
  , "private": "git+ssh://git@github.com:user/repo.git#ref"
}
```

---

```
$ npm init
```

---

```
$ npm version <major|minor|patch>
```

---

```
# Publish publicly!
# Get famous!
# Make friends!

$ npm publish
```

---

## Run scripts

`npm run <script-name>`

---

## Good idea

`npm run jshint`

---

# Browserify

---

> require(‘modules’) in the browser.

---

## Compatible with most Node modules
(~60k modules)

---

```
npm install browserify -g
```

---

## Already using AMD? SWitch!

https://github.com/thlorenz/browserify-ftw

---