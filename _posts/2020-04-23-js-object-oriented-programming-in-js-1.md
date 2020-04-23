---
layout: post
title: Object-oriented Programming in JS - 1
tags:
  - javascript
  - object-oriented
  - programming paradigms
  - object
  - class

---

**Object-oriented programming** (**OOP**) is a [programming paradigm](https://en.wikipedia.org/wiki/Programming_paradigm) based on the concept of "[objects](https://en.wikipedia.org/wiki/Object_(computer_science))", which can contain [data](https://en.wikipedia.org/wiki/Data), in the form of [fields](https://en.wikipedia.org/wiki/Field_(computer_science)) (often known as *attributes* or *properties*), and code, in the form of procedures (often known as *[methods](https://en.wikipedia.org/wiki/Method_(computer_science))*). A feature of objects is an object's procedures that can access and often modify the data fields of the object with which they are associated (objects have a notion of "[this](https://en.wikipedia.org/wiki/This_(computer_programming))" or "self"). In OOP, computer programs are designed by making them out of objects that interact with one another. OOP languages are diverse, but the most popular ones are [class-based](https://en.wikipedia.org/wiki/Class-based_programming), meaning that objects are [instances](https://en.wikipedia.org/wiki/Instance_(computer_science)) of [classes](https://en.wikipedia.org/wiki/Class_(computer_science)), which also determine their [types](https://en.wikipedia.org/wiki/Data_type).

### Fundamental Concepts of OOP

- [Classes](https://en.wikipedia.org/wiki/Class_(computer_science)) – the definitions for the data format and available procedures for a given type or class of object; may also contain data and procedures (known as class methods) themselves, i.e. classes contain the data members and member functions
- [Objects](https://en.wikipedia.org/wiki/Object_(computer_science)) – instances of classes
- Methods
- Properties
- Encapsulation
- Aggregation
- Inheritance
- Reuse

## Object

There is a soccer player called *Park Ji-Sung*. He can be defined with several characteristics like name, age, position and so on. He moves in games, i.e. dribbles, shoots etc. If he were an object in JS, his characteristics might be represented as properties and movement be method.

- Object: *Park Ji-Sung*
- Properties: name, age, height, position, current team ...
- Methods: dribble, shoot, pass, tackle ...

```javascript
var park_ji_sung = { 
	name: "Park Ji Sung",
	height: 178,
	weight: 70,
	position: "RW",
	team : "Queen’s Park Rangers"
};

console.log(park_ji_sung.team);
// "Queen’s Park Rangers"
```

## Class

Class is like mold casting, which makes many objects from one template. This can be explained with our soccer player class metaphor.

"*Park Ji-Sung* is an instance made from *Soccer Player* class"

And it is expressed in JS like this:

```javascript
var SoccerPlayer = function () { };

SoccerPlayer.prototype = { 
	name: String,
	age: Number,
	height: Number,
	weight: Number,
	position: String,
	team : String
};

var park_ji_sung = new SoccerPlayer(); 

park_ji_sung.name = "Park Ji Sung"; 
park_ji_sung.age = 31;
park_ji_sung.height = 178;
park_ji_sung.weight = 70;

console.log(park_ji_sung);
```

But the concept of OOP in JavaScript is slight **different** from C++ and JAVA. The concept of class does not actually exist in JavaScript. All elements in JS are **based on the object**.

JavaScript is a **prototypal** OOP language. 

"*Park Ji-Sung* is an instance made from *Soccer Player* class" should be rewritten like,

"*Park Ji Sung* is an object created with **reuse of the object *Soccer Player* as a prototype**"



<hr>

## Related Links

- [https://en.wikipedia.org/wiki/Object-oriented_programming](https://en.wikipedia.org/wiki/Object-oriented_programming)
- [https://edu.goorm.io/lecture/557/한-눈에-끝내는-node-js](https://edu.goorm.io/lecture/557/한-눈에-끝내는-node-js)