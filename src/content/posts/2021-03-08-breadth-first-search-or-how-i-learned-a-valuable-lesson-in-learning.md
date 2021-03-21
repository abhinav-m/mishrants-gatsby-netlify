---
template: blog-post
title: Breadth first search or how i learnt how to learn
slug: breadth-first-search-in-real-life
date: 2021-03-08 19:57
description: breadth first search, learning, productivity, efficiency,
  technology, passion, life, philosophy, shortest path, projects
featuredImage: /assets/bfs-upload.png
---
# Breadth first search - The shortest path ( subject to constraints ;) )



## A technical / philosophical overview:



> `Imagine a situation where you are standing on a road that diverges into 4 other roads. You are a skilled voyager, navigating through the harsh world, trying to reach your destiny. The only problem is ( and more so if you are like me), You don't know the path to your destiny!.`

``

**Worry not, breadth first search to the rescue!**



First a definition from [wikipedia](https://en.wikipedia.org/wiki/Breadth-first_search):

> <!--StartFragment-->
>
> **Breadth-first search** (**BFS**) is an [algorithm](https://en.wikipedia.org/wiki/Algorithm "Algorithm") for traversing or searching [tree](https://en.wikipedia.org/wiki/Tree_(data_structure) "Tree (data structure)") or [graph](https://en.wikipedia.org/wiki/Graph_(data_structure) "Graph (data structure)") data structures. It starts at the [tree root](https://en.wikipedia.org/wiki/Tree_(data_structure)#Terminology "Tree (data structure)") (or some arbitrary node of a graph, sometimes referred to as a 'search key'[](https://en.wikipedia.org/wiki/Breadth-first_search#cite_note-1)), and explores all of the neighbor nodes at the present depth prior to moving on to the nodes at the next depth level.
>
> <!--EndFragment-->



So if you are standing on a road, that diverges to 4 different roads, you would technically explore all of these different roads **UNTIL** you move on to the next set of roads (* **which would include all of the roads which were a part of the 4 roads you just explored***)



***BUT WHAT ARE THE ALTERNATIVES?***

*W**ell,*** If you are a books/podcasts/productivity junkie like me and you have read or heard up about the greats in their pursuit of their destiny (Think Michael Jordan, Roger Federer, Steve Jobs) etc. You might find a pattern to them that is common. 



>  All of these people had a relentless pursuit in their **craft**, and honed it with careful care and toil throughout their lives.



Now if you are a computer science nerd like me, the thought might arise, this sounds more like **DEPTH FIRST SEARCH** (DFS).

Again from [Wikipedia](https://en.wikipedia.org/wiki/Depth-first_search#:~:text=Depth%2Dfirst%20search%20(DFS),along%20each%20branch%20before%20backtracking.):

<!--StartFragment-->

> **Depth-first search** (**DFS**) is an [algorithm](https://en.wikipedia.org/wiki/Algorithm "Algorithm") for traversing or searching [tree](https://en.wikipedia.org/wiki/Tree_data_structure "Tree data structure") or [graph](https://en.wikipedia.org/wiki/Graph_(data_structure) "Graph (data structure)") data structures. The algorithm starts at the [root node](https://en.wikipedia.org/wiki/Tree_(data_structure)#Terminology "Tree (data structure)") (selecting some arbitrary node as the root node in the case of a graph) and explores as far as possible along each branch before backtracking.

<!--EndFragment-->

For the layman, depth first search is the exact opposite of the scenario described above with the roads: 

Given a choice of any 4 roads at a point and a destination, instead of exploring all 4 roads first, you take the first road ( or any of those 4 roads) and then subsequently you repeat this process until you reach ***a destination***.  

The only drawback to this approach ? Well:

> *The destination you reach might not be your destiny*



Does this mean that these people spent their entire life doing a **depth first search** in the pursuit of excellence without knowing their destiny?

Well, not really. 

Most of these athletes who compete at the highest level tend to start at a very early age during their childhood playing the sport they become veterans in.

 If the book by Malcom Gladwell has taught the world anything, its the **10,000** hour rule which can be summarized to :

>  You become the master of a craft of a field when you spend **10,000 hours of deliberate practice on** 



This *does* sound like a **depth first search in the pursuit of excellence**, where you traverse each **"dimension"** of your craft and hone it with the utmost care and consideration.

 For eg, a basketball player might work on his **vertical jump**, **his speed**, **his stamina**, **endurance, and any other skills** are related to his pursuit of excellence in the sport.



But before these accomplished people set out in a **depth first search** to **hone their craft**, they also did a quick **BFS** in their childhood **to pick their craft.**

**How ?**

* **Michael Jordan** engaged in all kinds of sports before basketball (football, baseball, etc), his favorite at a young age being baseball. 
* **Roger Federer**  also engaged in multiple sports in his childhood (badminton,basketball, etc) and redits his hand-eye coordination to the wide range of sports he played as a child, including badminton and basketball.
* The life of **Steve Jobs** is incredible to read about, and he dabbled in a lot of things before he founded apple and designed the first few revolutionary products which made that company.



## Breadth first search and learning:

Earlier when it came to the topic of learning something, i was incredibly ***naive* and aimed to be a perfectionist.**

My thought process would be something like:

1. Collect all the **BEST resources** to acquire this new skill and plan a path.

    For eg, I have been recently dabbling in data science , and for a huge portion of my time, i thought about revisiting all the prerequisite mathematics behind data science, then going through textbooks religiously, then actual projects / work in data science. (I come from a computer science engineering background, so this much preparation was  really not needed, When i actually started my pursuit, i just brushed up the topics i was confused about, or added them to a list which i need to look at later)
2.  Study these **resources scrupulously to gain knowledge**

   I remember trying to go through CLRS in one attempt or a C++ book by Bjarne Stroustrup during my college days. Boy was i wrong. These books are incredibly dense  and verbose, also i didn't have a good enough background of the basics to go through them at that time.
3. **Apply this knowledge to your domain.**

   Oh boy, spending all that time learning Java, then not building anything. (I love to build and create new stuff , thats why computer science intrigues me). All i got out of it was a small android app which i used in my major project! ( which i absolutely loved building and should have started working on earlier, where i could have improved it a lot)