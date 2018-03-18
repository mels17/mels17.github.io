---
layout: post
title: Javascript - A journey into the unknown
---

The last post was written a month before. Well, I would have been more regular in writing posts if not for Javascript and since it has been a long time after my last post, please bear with my random and disoriented ramblings. A week of learning Kotlin and I have switched to learning another language. You may think - Was kotlin that hard or did I just get bored? The answer is neither. You see, the top three languages used in MYOB is Java, JavaScript and C#. So I though, JavaScript is really close to Kotlin, so I should learn that first.

### Programming Horror Stories - Chapter 2

Starring: Javascript, Sublime/Atom, Terminal, Jasmine

On a completely normal day, I was about to test the code I had written so far. I pressed the green play button on the right-hand side of Webstorm, crossing my fingers at the same time and hoping that I see all green! But it came up with an error "cannot read property of undefined". I retraced my code-steps - function-by-function I debugged my code, but I could find nothing wrong with it. All the objects and promises passed were defined and I made sure it was by using console.logs. You see I had to manually debug my program as I couldn't get the Webstorm debugger with Jasmine working. Well, anyways, I spend hours on end to debug but couldn't find anything wrong. I went to my mentor, Andrew, with this error and he just needed a quick glance to tell me that I didn't actually return the value. 

That came as a complete surprise to me. My eyes zoomed in on the empty space where the keyword return should have been. I was 100% sure that I had written it there. If this was the first time that it happened to me, I wouldn't have given it a serious thought, but this was the second time...

```Cause```: I can only think of three ways this could have happened:


### Programming Horror Stories - Chapter 3

Starring: Jasmine, Webstorm and JavaScript

