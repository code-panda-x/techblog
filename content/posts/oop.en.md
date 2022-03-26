---
title: "What is OOP"
date: 2022-02-01T21:08:59-05:00
draft: false
tags: ["OOP", "What is"]
categories: ["General Tech"]
slug: "oop"
subtitle: "OOP Ideas"
description: "OOP Ideas"
keywords: 
- Encapsulation
- Inheritance
- Polymorphism
- OOP
---

### Class
Blue print of the objects

### Object
An object is an instance of a class (Class -> blueprint, Object -> house)

### Constructor
Initialize the state of an object

### Destructor
Automatically called at the end of lifetime of an object
Free up the acuired resources

### Is-A Relationship 
Inheritance (Parent-Child) 

	class Apple extends Fruit {
	}

Foo is-a Bar:

	public class Foo extends Bar{}


### Has-A Relationship 
Composition: Creating instances which have references to other objects (Objects depend on each other) 

	class Room {
    Table table = new Table();
	}

Foo has-a Bar:

	public class Foo {
  	  private Bar bar;
	}

### Association Relationship 
Has-A(Own Life Time | Exists Independently/Isolation) 
eg. Manager has a Swipe Card

### Aggregation Relationship
Has-A(Ownership | Single owner of Child Object | Child Objects can exists Independently) 
eg. One Manager - Many Workers


### Abstraction 
Exposing only the relevant details of an entity

**A class can extend multiple abstract classes**

### Encapsulation 
Binding data and operations together in an entity

- Information hiding: Access control modifier
- Implementation hiding: Through creation of interface for class

### Diffrence between abstraction and encapsulation
Abstraction: The concept of allowing the user of your class to have access to only what they need. (Concept) 

Encapsulation: The physical code that prevents the user from accessing fields or methods you do not want them to (Actual Implementation) 


### Inheritance
- Reusability of code
- Inheriting characteristics from parent class to child class without modifications

### Polymorphism:
An object can have different forms
- Static polymorphism: method overloading
- Dynamic polymorphism: method overriding

Example:

```
abstract class Animal {
	String name;

	//cool functionality
	abstract String bark();
}

// Inheritance
class Dog extends Animal {
	String bark() {
		return "Bow Bow";
	}
}

class Cat extends Animal {
	String bark() {
		return "Meow Meow";
	}
}

public class InheritanceExamples {
	public static void main(String[] args) {
		Animal animal = new Cat();
		System.out.println(animal.bark());
	}
}
```

### Method Overloading vs Overriding
Overloading:
Same name but **different parameters**

Overriding:
Same name and **same parameters**

![overloading-vs-overriding.png](/images/overloading-vs-overriding.png)

### Abstract class
Abstract class is a half-defined parent class. Needs to be extened and methods implemented

**Can't** be instantiated

User is not told about the process but only the method about the class (single approach)

    public abstract class Customer
    {
        public abstract decimal Discount();
    }

    public class richCustomer : Customer
    {
        public override decimal Discount();
    }


### Interfaces
A class with **no implementation**

It contains only the **declaration** of methods, parameters and values

```
interface Flyable {
	void fly();
}

class Aeroplane implements Flyable {
	public void fly() {
		System.out.println("Aeroplane is flying");
	}
}

class Bird implements Flyable {
	public void fly() {
		System.out.println("Bird is flying");
	}
}

public class InterfaceExamples {
	public static void main(String[] args) {
		Flyable flyable = new Bird();
		flyable.fly();
	}
}
```


### Interface vs Abstract class
![interface-vs-class.png](/images/interface-vs-class.png)
Fist interface created, then abstract class, then concrete classes

![interface-vs-class2.png](/images/interface-vs-class2.png)


### Early binding vs Late binding
![binding.png](/images/binding.png)

