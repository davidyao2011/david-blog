---
title: Data Structures and Algorithms (Part 1)
date: "2017-06-06T23:46:37.121Z"
---
## Overview and Objectives

![data structures](./data.jpg)
####1.Understand abstract data types stack, queue, deque, and list. 
####2.Implement arrays, ArrayLists and LinkedLists in Java programming language
####3.mplement the stack, queue, and deque Abstract data types in Java programming language.
####4.Understand the Tree and Set data structures
####5.To understand the performance of the implementations of basic data structures.
####6.To be able to select appropriate data structure for given scenarios.
####7.Apply coding standards

### Arrays
####Introduction
One of the main concepts in software development is working with data structures to store and retrieve data. Arrays are one of the most fundamental data structures, they can be found in most programming languages, including Java. In addition to standard arrays, Java has an ArrayList class that is included in its software development kit (SDK). The ArrayList class follows the principles of Object-Oriented programming to represent arrays. Below you will learn about both arrays and ArrayLists, their advantages and weak sides.

Arrays are Java's most basic and commonly used data structure. They can be thought of as a group of variables. 

####Multi-Dimensional Arrays
Arrays do not need to be restricted to a single dimension. As useful as one-dimensional arrays are, arrays of higher dimensions are commonly used as well and can add a whole new level of functionality to your data storage. Whereas a single-dimensional array can be thought of as a list, or a table with only one row, a two-dimensional array can be thought of as a table with multiple rows and columns.

An example of two-dimensional array could be an array storing students' grades over the course of their study. Each row will represent specific course and each column will represent specific assessment grade. For this example let's assume that each student studies four courses and that each course has three assessments to complete.

###ArrayLists
####ArrayLists
Arrays are common in programming, and there are a number of common operations that must be performed on them. Two of the most common are insertion and deletion (adding and removing elements). However, this is where the limitations of arrays become readily apparent:

If you want to resize an array keeping the current elements in Java, you have to make another array then copy the contents of the old array to the new array.
If you want to remove an element from an array, you have to make a copy of the element and then shuffle all the trailing elements up by one place. This however leaves you with two copies of the last element.

If you want to insert an element into an array, you have to shuffle the elements down by one place to make a free slot. This however then requires you to recreate the array by adding one the the size of the array. And then if you wish to add an element at a certain position even more work is required.

An ArrayList is slightly different from an array in that it stores its elements as objects instead of primitive types (ints, bools, etc). An Object type is the most common type in Java framework from which all other types are built on. This means that any type can be stored in a variable of type Object allowing ArrayList to consist of more than one type.


###Pros and Cons of Arrays and ArrayLists
As with any tool, your best bet is to use the one that fits the job. In most general cases, the ArrayList is likely to be easier to work with. It allows for growing and shrinking data sets, allows elements to be added or removed at any valid index, and offers many more methods that make working with ArrayList easier.

However, if the size of the data is known, then the automatic expanding and shrinking feature of ArrayList is not needed. If primitives must be used, then the standard array must be used.

##ArrayLists
###Advantages:

Automatically resizes when capacity is exceeded.
Objects can be placed in the middle of the ArrayList and it will readjust all other elements.
Objects can be easily removed from anywhere in the ArrayList and all other elements will automatically readjust.
ArrayLists implement the List interface, so can be used in a loosely coupled manner (easily changed to another type of List if necessary).
As ArrayList stores Object types, if desired, ArrayList can contain elements of different Object data types.
###Disadvantages:

Cannot store primitives without being in wrapper class, for example stores Integer, not int, Boolean, not boolean, etc.
Extra overhead is required when it is resized.
Must nest multiple ArrayLists in an ArrayList to work similar to a multi-dimensional array, without having an elegant mechanism to refer to the elements.

###Arrays
###Advantages:

Can store primitive values.
No overhead to access data.
Easy to create multi-dimensional arrays.
###Disadvantages:

Cannot be resized.
When adding or removing data, the array must be managed manually.