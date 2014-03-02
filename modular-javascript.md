> “Absorb what is useful, discard what is not, add what is uniquely your own.”
~ Bruce Lee

-------------------------------------

# Modular JavaScript With npm and Node Modules

_Eric Elliott_

-------------------------------------

![adobe](https://f.cloud.github.com/assets/364727/2303817/4b9a55dc-a1e8-11e3-874f-74118b6e28c7.jpeg)

![tout](https://raw.github.com/dilvie/fluent-prototypal-oo/master/tout.jpg)
 ![bandpage](https://raw.github.com/dilvie/fluent-prototypal-oo/master/bandpage.jpg)
 ![zumba](https://raw.github.com/dilvie/fluent-prototypal-oo/master/zumba.jpg)

-------------------------------------

![Programming JavaScript Applications](http://akamaicovers.oreilly.com/images/0636920033141/lrg.jpg)

-------------------------------------

# Why Modules?

-------------------------------------

## DRY (Don't Repeat Yourself)

-------------------------------------

## Stay Organized

-------------------------------------

## Maintain Separation of Concerns

-------------------------------------

## Domain logic

-------------------------------------

## Presentation

-------------------------------------

# Different Modules

-------------------------------------

# Why Node Style Modules?

-------------------------------------

## Stupid Simple Syntax

-------------------------------------

### Export Something

```js
'use strict'; // You should always do this.

var foo = function () {
  return true;
};

module.exports = foo;
```
-------------------------------------

### Import Something

```js
var foo = require('./foo.js');

foo(); // true
```

-------------------------------------

## Unbeatable ecosystem

![module-counts](https://f.cloud.github.com/assets/364727/2303815/1a87865e-a1e8-11e3-83e7-29704df31738.png)

-------------------------------------

## Great Package Management

-------------------------------------

## Keep all modules in Git

-------------------------------------

## Version using semver

major.minor.patch

-------------------------------------

* major = breaking changes
* minor = new non-breaking features
* patch = bug fixes, insignificant changes

-------------------------------------

# Principles of Modularity

Modules should be:

-------------------------------------

## Specialized

DOT (Do One Thing)

-------------------------------------

## Independent

* Do something useful independent of the app.
* Don't grab stuff from globals.

-------------------------------------

## Decomposable

* You should be able to test your modules outside your app.
* Like component entertainment center.

-------------------------------------

## Recomposable

* Should be possible to rearrange the modules to build a different app.

-------------------------------------

## Substitutable

* You should be able to swap out one module for another, as long as they share the same public interface.

-------------------------------------

## Open / Closed

Open to extension, closed to modification

-------------------------------------

# Interfaces

> "Program to an interface, not an implementation."

~ The Gang of Four, "Design Patterns: Elements of Reusable Object-Oriented Software"

-------------------------------------

## Interface is a Contract

* Enables substitution

-------------------------------------

## Obey the Open / Closed Principle

-------------------------------------

## Export Your Public API

-------------------------------------

## Encapsulate Your Implementation

* Easy - just don't export it!

-------------------------------------

## KISS (Keep It Simple, Stupid)

-------------------------------------

## Keep It Stupid Simple

-------------------------------------

## Export One Function

-------------------------------------

## Don't Export Constructors

-------------------------------------

## Do Export Factories

-------------------------------------


> It’s not the daily increase but daily decrease. Hack away at the unessential.
~ Bruce Lee

-------------------------------------

