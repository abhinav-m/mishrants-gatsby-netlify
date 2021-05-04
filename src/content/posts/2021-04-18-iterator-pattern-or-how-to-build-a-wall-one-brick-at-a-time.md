---
template: blog-post
title: Iterator pattern - or how to build a wall, one brick at a time.
slug: iterators-or-how-not-to-worry-and-start-living
date: 2021-04-18 19:50
description: >
  Michael Jordan , in the popular documentary "The Last Dance" by Netflix , says
  something that would feel uncomfortably familiar to most of us, yet we don't
  seem to follow it.


  Why would I worry about a shot that I haven't taken yet?


  Seneca, the great roman stoic philosopher also had a quote about worrying about the future:


  He suffers more than necessary, who suffers before it is necessary” — Seneca


  A few weeks ago, I was reading about the popular design pattern used in programming languages everywhere known as the iterator pattern which struck me as philosophical in nature.
---
**Michael Jordan** , in the popular documentary "The Last Dance" by Netflix , says something that would feel uncomfortably familiar to most of us, yet we don't seem to follow it.

> **Why** would I worry about a shot that I haven't taken yet?

**Seneca,** the great roman stoic philosopher also had a quote about worrying about the future:

> He **suffers more** than necessary ,**who suffers before** it is necessary” — Seneca

Will Smith, the successful Hollywood actor has a very famous interview on YouTube where he explains his philosophy about his work:

> You don't set out to **build a wall**. You **don't say I'm going to build the biggest, baddest, greatest wall** that's ever been built. You don't start there. You **say I'm gonna lay this brick as perfectly as a brick can be laid** and you do that **every single day**, **and soon you have a wall.**

A few weeks ago, I was reading about the popular design pattern used in programming languages ubiquitously known as the [iterator pattern](https://en.wikipedia.org/wiki/Iterator_pattern) which struck me as philosophical in nature.

The design pattern, itself is quite simple:

Here's an example of the pattern using JavaScript and [Symbols](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol) .

```javascript
function range(start, end) {
  return {
    [Symbol.iterator]() { // #A
      return this;
    },
    next() {
      if (start < end) {
        return { value: start++, done: false }; // #B
      }
      return { done: true, value: end }; // #B
    }
  }
}

for (number of range(1, 5)) {
  console.log(number);   // -> 1, 2, 3, 4
}
```

If you are unfamiliar with JavaScript, the above `range`function, does exactly what the python range function does, generate numbers in the range of`1 - 5` (end exclusive)

Here's the same code written using Java:

```java
import java.util.Iterator;
import java.util.NoSuchElementException;

public class RangeIteratorExample {
    public static Iterator<Integer> range(int start, int end) {
        return new Iterator<>() {
            private int index = start;
      
            @Override
            public boolean hasNext() {
                return index < end;
            }

            @Override
            public Integer next() {
                if (!hasNext()) {
                    throw new NoSuchElementException();
                }
                return index++;
            }
        };
    }
    
    public static void main(String[] args) {
        var iterator = range(0, 10);
        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }
        
        // or using a lambda
        iterator.forEachRemaining(System.out::println);
    }
}
```

And just to make the concept stick, Here's an iterator written in JavaScript, that iterates through an array in reverse, using an object.

```javascript
function reverseArrayIterator(array) {
    var index = array.length - 1;
    return {
       next: () =>
          index >= 0 ?
           {value: array[index--], done: false} :
           {done: true}
    }
}

const it = reverseArrayIterator(['three', 'two', 'one']);
console.log(it.next().value);  //-> 'one'
console.log(it.next().value);  //-> 'two'
console.log(it.next().value);  //-> 'three'
console.log(`Are you done? ${it.next().done}`);  //-> true
```

All of these examples have been taken from [Wikipedia](https://en.wikipedia.org/wiki/Iterator_pattern), and the design pattern itself is used extensively throughout  multiple programming languages. But how does it tie into philosophy?

Well, iterators can represent real life in a lot of ways.

Let us try to think of what iterators do in a way that represents real life.

In the above **range iterators example,** we are generating a sequence of numbers (end exclusive) where the numbers themselves are not generated *beforehand.*  Taking a more philosophical look at this, I like to think of iterators as working on something one thing (*or brick if you have been reading closely)* at a time. 

Iterators ***do not worry*** about the **future, or the past**. All they care about is the present. In the range iterators example, the iterator has the current value of the range, until it's done condition is reached. In the **reverseArrayIterator** just above, the iterator only cares about the current index of the array, starting from the last index.