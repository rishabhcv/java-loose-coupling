# java-loose-coupling

A simple Java application demostrating the concept of loose coupling by using interfaces and their implementations.

## The Purpose

The purpose of this Java application is to show how we can make the functionality of an application loosely coupled. The aim is to move from this type of loose coupling where we have to instantiate new objects, to Spring where we can use annotations and forget about instantiation altogether. 

## What's happening here?
We have to run our BinarySearch algorithm but the array we have is not sorted. We have the option to use various algorithms for the sorting part. What can we do? 

#### Approach 1: Tight Coupling
We can make the sorting algorithms in two different classes and call them in the BinarySearchImpl's method to sort. We will have to use the *sort()* method to do that, which can be done by instantiating the sorting class we want to use and then call its sort() method.

#### Approach 2: Loose Coupling
Now to avoid instantiating a specific class in the BinarySearchImpl class, we can create an interface, have the sorting methods implement it and then make a constructor in BinarySearchImpl and pass a new object of the sorting algorithm we want. This way, we have eliminated the tight coupling between the BinarySearchImpl class and the other sorting classes.

