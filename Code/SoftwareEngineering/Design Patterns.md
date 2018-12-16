# Design Patterns

### Intro:
###### Simple OO
```
Class: Duck{
	swim()
	display()
	fly()
	quack()
}
```
Problem:   
Class RubberDuck extends Duck -> inherits fly

Solution:
```
Interface Flyable{
	fly()
}   
```
Problem:   
1) All subclasses have to implement the Interface as there is no implementation in Java   
2) Any change in fly should be implemented in all its sub class   


Design Principle:   
Take what varies and **Encapsulate** so it wont affect the rest of your code   
Result: few unintended consequences from code changes and more flexibility  

Design Principle:   
Program to interface not a implementation
