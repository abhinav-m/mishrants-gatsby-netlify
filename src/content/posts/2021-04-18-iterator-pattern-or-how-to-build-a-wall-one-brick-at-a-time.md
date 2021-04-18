---
template: blog-post
title: Iterator pattern - or how to build a wall, one brick at a time.
slug: iterators-or-how-not-to-worry-and-start-living
date: 2021-04-18 19:50
description: >+
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

> He **suffers more** than necessary,**who suffers before** it is necessary” — Seneca

A few weeks ago, I was reading about the popular design pattern used in programming languages ubiquitously known as the [iterator pattern](https://en.wikipedia.org/wiki/Iterator_pattern) which struck me as philosophical in nature.

The design pattern, itself is quite simple:



Here's an example of the pattern using Javascript and [Symbols](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol) .

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



If you are unfamiliar with Javascript, the above `range `function, does exactly what the python range function does, generate numbers in the range of`  1 - 5 ` (end exclusive)



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



And just to make the concept stick, Here's an iterator written in Javascript, that iterates through an array in reverse, using an object.

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