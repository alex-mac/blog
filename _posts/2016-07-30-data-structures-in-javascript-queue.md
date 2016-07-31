---
layout: post
title:  Data Structures in Javascript: Queue
date:   2016-07-30 06:58:00 -0800
---

Sorry for the long break since my last post! I have been learning a lot and working very hard at my work! As a short status update, I am in charge of a huge project in which I am converting a manual process for veteran students and making the experience completely online. I have also been studying Java and learning about simple data structures, something which we didn't spend too much time on while in class during my time at General Assembly. Now, I am starting a series to help augment codeschool students and help them understand simple data structures in Javascript!

Today, I'll be introducing a data structure known as a Queue. In Web Development (or in my experience with it thus far), there is not a strong need to understand data structures. You can get awawy with not understanding data structures at all, actually. For example, a Queues and Stacks can be implemented with an array. I do believe however that understanding and mastering different types of data structures will allow you to become a better programming and think more critically about a problem. Especially with the introduction of classes in ES6, the abstraction and encapsulation of data can help other developers understand code much more quickly and easily. 

A Queue is a data structure that contains data in First In First Out (FIFO) order. You can think of a line at the bank or, if you're not from America, you probably refer to a line as a queue anyways. Items that enter the queue first are processes first. 

When working with a Queue, you can add items to the queue, remove items from the front of the queue and print out your queue.

In Javascript, you can use an array to create a queue without ever using a class: 

{% highlight javascript %}
  var queue = [1,2,3,4,5];

  // queue.add
  queue.push(6); // queue = [1,2,3,4,5,6]

  //queue.remove
  queue.shift(); // queue = [2,3,4,5,6]

  console.log(queue) // [2,3,4,5,6]
{% endhighlight %}

An array has all the methods you would need to implement a queue. Now I'm going to go into a little bit more details on how to create a queue class in es6.

{% highlight javascript %}
  // A queue stores a collection of data in FIFO order. A queue can add items to the queue, remove items from the front of the queue, peek at the first item in the queue, and get the size of the collection.
  class Queue {

    // constructs an empty queue to store data
    constructor() {
      this._data = [];
    }

    // adds a value to the end of this queue
    add(value) {
      this._data.push(value);
    }

    // removes the first value in this queue
    remove() {
      this._data.shift();
    }
    
    // returns the front most item of this queue
    peek() {
      return this._data[0];
    }

    // returns the size of this queue.
    size() {
      return this._data.length;
    }
  }
{% endhighlight %}

Although it may seem silly to have a class where every method executes exactly one line of code, the most important concept is here that this Queue class abstracts the data and makes the queue a lot more user friendly. When reading foreign code, it is a lot nicer to read and understand than looking at several arrays. As you can see, a queue is a pretty simple data structure, especially in a language like JavaScript where an array handles data in the same way!