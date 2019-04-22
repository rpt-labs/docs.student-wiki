## Technical Interview Reference Questions

#### What is a reference question?

A reference question, as opposed to an experience of performance question, is a factual question asked with the intention of gauging your understanding of a certain programming language's design and syntax. There is typically only one correct answer to these questions and they are often asked during a phone screen, or in the beginning of an on-site interview. There are two different types of reference questions: (1) Conceptual questions that can be answered entirely verbally, and (2) evaluating code snippets that might feature some of the trickier parts of the language. This document will provide examples of each type of question.

#### How to get the most value out of this document

You should use this document as a learning tool to check in with yourself. Run through the questions provided and see if you can come up with an answer to each of them. Grab a partner and tell him your answer. If you find yourself answering clearly and concisely, you're on a good track. If you find yourself providing long-winded answers or struggle to even find an answer, use the suggested resources section below to brush up these concepts, and try to come up with a more concise answer. The linked resources have been vetted carefully to make sure they contain high quality information.

### List of questions

Focus on communicating these concepts to someone else. Often times you'll find that you have a very good understanding of a concept, but struggle communicating it. Clear communication is critical during interviews.

- [Javascript fundamentals](#javascript-fundamentals)
- [Back-end specific](#back-end-specific)
- [Front-end specific](#front-end-specific)
  - [HTML](#htmldom)
  - [CSS](#css)

#### Javascript fundamentals

* How does inheritance work in Javascript?
* What kind of scope do variables have?
* What is a closure?
* What is function hoisting?
* What is variable hoisting?
* What does the keyword 'new' do?
* How does the keyword 'this' work?
* Can you explain event delegation?
* How would you use an arbitrary object as value of 'this'?
* What is the difference between 'call' and 'apply'? What are their purposes?
* Does JavaScript pass parameters by value or by reference?
* What are the differences between == and ===?
* What are the differences between null and undefined?
* What are the different JavaScript data types?
* What is an immediately invoked function expression (IIFE)? Why would you want to use one?
* What's a typical use case for anonymous functions?
* What is a potential pitfall with using typeof bar === "object" to determine if bar is an object? How can this pitfall be avoided?
* What is the significance, and what are the benefits, of including 'use strict' at the beginning of a JavaScript source file?
* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
* What does it mean for a property on an object to be enumerable?
* What is the difference between a native object and a host object?
* Why is extending built in JavaScript objects not a good idea?
* Why might a programmer have defined a variable with a capital letter?
* What is JSONP? When would you use it?
* What is the difference between asynchronous code and concurrent code?


#### Back-end specific

* What is a document database?
* Explain the difference between a SQL database and a document database.
* What does the `3000` mean in http://localhost:3000 and why might we sometimes specify them in URLs.
* What are REST and RESTful endpoints?  Give examples.
* What is XSS?
* List the four main HTTP verbs and describe how they are used.
* What are sockets?  When might you use them.
* What is the `event loop`?  How does it handle... synchronous calls, asynchronous calls.
* What is a foreign key?
* Why are indexes in databases useful?  (What is an index?)
* What does does it mean to secure data "in transit" and "in place"?

#### Front-end specific

Although we don't focus too much on these nuances in our curriculum, our alumni have reported that it's common for front-end interviews to include some variety of HTML/CSS questions. Check out the resources below if you're very interested in a front-end position and feel rusty in any of these areas.

#### HTML/DOM

* How do you serve a page with content in multiple languages?
* What kind of things must you be wary of when design or developing for multilingual sites?
* What are `data-` attributes good for?
* Describe the difference between a cookie, sessionStorage and localStorage.
* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
* Why is it generally a good idea to position CSS `<link>` between `<head></head>` and JS `<script>` just before `</body>`? Do you know any exceptions?
* What's the difference between an attribute and a proprety?
* What are different ways to get an element from the DOM (without jQuery)?

#### CSS

* What is the difference between classes and IDs in CSS?
* What is the difference between 'resetting' and 'normalizing' CSS? Which would you choose, and why?
* What are psuedo-classes?
* Describe floats and how they work.
* Describe z-index and how stacking context is formed.
* What are the various clearing techniques and which is appropriate for what context?
* How would you approach fixing browser-specific styling issues?
* How do you serve your pages for feature-constrained browsers?
* Have you ever used a grid system, and if so, what do you prefer?
* Have you used or implemented media queries or mobile specific layouts/CSS?
* What are the advantages/disadvantages of using CSS preprocessors?
* Describe what you like and dislike about the CSS preprocessors you have used.
* Explain how a browser determines what elements match a CSS selector.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does `{ box-sizing: border-box; }` do? What are its advantages?
* What's the difference between inline and inline-block?
* What's the difference between a relative, fixed, absolute and statically positioned element?
* The 'C' in CSS stands for Cascading. How is priority determined in assigning styles (a few examples)? How can you use this system to your advantage?
* Have you played around with the new CSS Flexbox or Grid specs?

### Tricky javascript code snippets

In addition to just conceptual questions, reference questions can include parsing a snippet of code to determine the correct output. Usually these snippets include some JavaScript nuance that makes the first glance answer incorrect.

These questions test your knowledge of these nuances, and for JavaScript usually include concepts like scoping, function expressions (versus functions declarations), references, order of evaluation, hoisting, and object instantiation.

The [Perfection Kills Quiz](http://perfectionkills.com/javascript-quiz/) is a great example of these types of questions. If you get a question wrong, play around with it in the console to try and uncover what where your expectations diverged from reality. You might learn something new.

If you get really stuck, HR20 alum Anastasia Zotova wrote a solution guide to the quiz. You can find it [here](http://anastasiazotova.com/perfection-kills-quiz-part-1/)

### Resources with answers to reference questions

The answers to all of the reference questions (and more) can be found in the following resources. There may certainly be overlap in the content covered - that just means more practice! Without further ado, here are our recommended resources:

#### Javascript Fundamentals

* All of the HR lecture slide decks and self guided lessons! Tons of hours have been put into these slide decks to make them as comprehensive as possible. Now is an amazing time to refresh your memory on some of their details. Head over to [Learn2](http://learn.makerpass.com) to start reviewing.
* [JavaScript garden](http://bonsaiden.github.io/JavaScript-Garden/) is a growing collection of documentation about the most quirky parts of the JavaScript programming language.
* [You don't know JS](https://github.com/getify/You-Dont-Know-JS) is a book series that dives deep into JavaScript. You can pay for the book if you like, but the author also put every chapter on github (linked here). Some of the chapters go beyond the questions above and into areas like async, performance, ES6, and more.
* Even though there weren't any specific questions above, you should definitely be comfortable with time complexity and basic data structures. For time complexity, check out [The Big O Cheat Sheet](http://bigocheatsheet.com/) and [Interview Cake](https://www.interviewcake.com/big-o-notation-time-and-space-complexity). For data structure practice, Wikipedia is unmatched.

#### Back-end specific

* [XSS](http://en.wikipedia.org/wiki/Cross-site_scripting)
* [HTTP Methods for RESTful services](http://www.restapitutorial.com/lessons/httpmethods.html)
* [Understanding the event loop](http://2014.jsconf.eu/speakers/philip-roberts-what-the-heck-is-the-event-loop-anyway.html)
* [SQL vs NoSQL](http://www.mongodb.com/nosql-explained)
* [Foreign keys](http://en.wikipedia.org/wiki/Foreign_key)
* [Node School - learn about the Node ecosystem](http://nodeschool.io/)
* [Node Streams](http://nodejs.org/api/stream.html)

#### Front-end specific

MDN is the best place for detailed information about the DOM, HTML, and CSS. The introduction pages liked here are a great place to start your exploration.
* [The DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
* [HTML](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Introduction)
* [HTML5](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
* [CSS](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started)
* [CSS3](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS3)
