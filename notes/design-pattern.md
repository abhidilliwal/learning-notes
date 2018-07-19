# Design Patterns 2018

## The Strategy pattern

 > In short: Prefer composition over inheritance.

With Object Oriented programming sometimes we overuse inheritance. for example if the base class is implementing too many things, then in subclasses you need to either override some stuff.

In Inheritance you first see what properties are highly unlikely to change, only those properties/methods should go in the BaseClass.

![0.xe5cgc0g8h9](/:storage/0.xe5cgc0g8h9.png)

In above diagram, Duck is the base class but it does not have the flying method implemented in it, coz it might change with sub-classes, so here we moved it to its own interfaces, which implements its own way of flying `flyWIthWings` and `FlyNoWay` in this way the subclass can choose implementation.


in JS we can do composition by just attaching to prototype. this way we can re-use the same function.

```js

function flyWithWing() {
  // some implementation
  console.log('flying with wing');
}


function Bird () {
  // ...
}

Bird.prototype.fly = flyWithWing;



function FlyingDuck () {
  // ...
}

FlyingDuck.prototype.fly = flyWithWing;

```


## Observer pattern

It defines 1-to-many relationships between `Publisher` and `Subscribers`.

 - Loosely coupled, Publisher and Subscriber.
 - They can exist without each other.

We use it a lot in JS apps.



