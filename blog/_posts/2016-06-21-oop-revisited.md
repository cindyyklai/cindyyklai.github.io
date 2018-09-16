---
id: 277
title: OOP revisited
date: 2016-06-21T17:03:26+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=277
permalink: /index.php/2016/06/21/oop-revisited/
categories:
  - Programming
  - Technology
---
## Classes

Classes are a way of describing the blueprint of an object.

## Fundamental principles of OOP

1) Abstraction
  
2) Polymorphism
  
3) Inheritance
  
4) Encapsulation

## Inheritance

Allows a class to override or extend the functionality of a base class.

## Abstraction

Allows complex logic to be abstracted out. Achieved using interfaces and abstract classes.

### Abstract classes

&#8211; Cannot be instantiated.
  
&#8211; It defines or partially implements the methods for any class that extends it.
  
&#8211; An abstract method cannot have an implementation.
  
&#8211; Any class that inherits from an abstract class, all abstract methods must be implemented by the derived class or they must be declared abstract.
  
&#8211; Unlike interfaces, abstract classes may have methods with full implementation and may also have defined member fields. 

### Interface

&#8211; An interface is not a class.
  
&#8211; Interfaces join types that are unrelated.
  
&#8211; Can only define method names, has no implementation.
  
&#8211; Any class that implements an interface must implement all the methods it defines or it must be declared abstract.

### Difference between abstraction and interface

Abstract classes allow you to partially implement your class, whereas interfaces contain no implementation for any members.

## Encapsulation

Encapsulation hides the implementation details of a class from the object. In Encapsulation, the data is not accessed directly; it is accessed through the functions present inside the class. In simpler words, attributes of the class are kept private and public getter and setter methods are provided to manipulate these attributes. Thus, encapsulation makes the concept of data hiding possible.

## Polymorphism

Polymorphism is the process of using function in different ways for different object types (method overriding).

A class can implement many interfaces and inherit only one class (even if that class is abstract)

Excellent article on PHP OOP:
  
http://zetcode.com/lang/php/oopi/
  
http://www.introprogramming.info/english-intro-csharp-book/read-online/chapter-20-object-oriented-programming-principles/#_Toc362296568 (For C# but the concepts are the same)