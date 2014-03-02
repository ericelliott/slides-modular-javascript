> “Absorb what is useful, discard what is not, add what is uniquely your own.”
~ Bruce Lee

-------------------------------------

# Modular JavaScript With npm and Node Modules

_Eric Elliott_

-------------------------------------

![Adobe Logo](adobe.jpeg)

![Tout](tout.jpg) ![BandPage](bandpage.jpg) ![Zumba Fitness](zumba.jpg)

-------------------------------------

!["Programming JavaScript Applications"](pja.jpg)

-------------------------------------

# Why Modules?

-------------------------------------

## DRY (Don't Repeat Yourself)

-------------------------------------

## Stay Organized

-------------------------------------

## Maintain Separation of Concerns

* Domain logic
* Presentation

### Different Modules

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

### Unbeatable ecosystem

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

## Export Your Public API

-------------------------------------

## Encapsulate Your Implementation

* Easy - just don't export it!

-------------------------------------

## KISS (Keep It Simple, Stupid)

-------------------------------------

## Keep It Stupid Simple?

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

