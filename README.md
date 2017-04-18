# Front-end quiz

## HTML
 
- [ ] What does a ```doctype``` do?
- [ ] What's the difference between full standards mode, almost standards mode and quirks mode?
- [ ] What's the difference between HTML and XHTML?
- [ ] Are there any problems with serving pages as ```application/xhtml+xml```?
- [ ] How do you serve a page with content in multiple languages?
- [ ] What kind of things must you be wary of when design or developing for multilingual sites?
- [ ] What are ```data-``` attributes good for?
- [ ] Consider HTML5 as an open web platform. What are the building blocks of HTML5?
- [ ] Describe the difference between a ```cookie```, ```sessionStorage``` and ```localStorage```.
- [ ] Describe the difference between ```<script>```, ```<script async>``` and ```<script defer>```.
- [ ] Why is it generally a good idea to position CSS ```<link>```s between ```<head></head>``` and JS ```<script>```s just before ```</body>```? Do you know any exceptions?
- [ ] What is progressive rendering?
- [ ] Have you used different HTML templating languages before?
- [ ] What were some of the key goals and motivations for the HTML5 specification?
- [ ] What are some of the key new features in HTML5?
- [ ] What are “web workers”?
- [ ] How do you indicate the character set being used by an HTML5 document? How does this differ from older HTML standards?
- [ ] Discuss the differences between an HTML specification and a browser’s implementation thereof.
- [ ] Briefly describe the correct usage of the following HTML5 semantic elements: ```<header>```, ```<article>```, ```<section>```, ```<footer>```.
- [ ] Can a ```<section>``` contain ```<article>``` elements? Can an ```<article>``` contain ```<section>``` elements? Provide usage examples.
- [ ] Can a web page contain multiple ```<header>``` elements? What about ```<footer>``` elements?
- [ ] Describe the relationship between the ```<header>``` and ```<h1>``` tags in HTML5.
- [ ] Give a simple implementation of the ```<video>``` tag to embed a video stored at http://www.example.com/amazing_video.mp4. Give the video a width of 640 pixels by 360 pixels. Provide the user with controls.
- [ ] Write the code necessary to create a 300 pixel by 300 pixel ```<canvas>```. Within it, paint a blue 100 pixel by 100 pixel square with the top-left corner of the square located 50 pixels from both the top and left edges of the canvas.
- [ ] What is HTML5 Web Storage? Explain localStorage and sessionStorage.

## CSS

- [ ] What is the difference between classes and IDs in CSS?
- [ ] What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
- [ ] Describe Floats and how they work.
- [ ] Describe z-index and how stacking context is formed.
- [ ] Describe BFC(Block Formatting Context) and how it works.
- [ ] What are the various clearing techniques and which is appropriate for what context?
- [ ] Explain CSS sprites, and how you would implement them on a page or site.
- [ ] What are your favourite image replacement techniques and which do you use when?
- [ ] How would you approach fixing browser-specific styling issues?
- [ ] How do you serve your pages for feature-constrained browsers?
  - [ ] What techniques/processes do you use?
- [ ] What are the different ways to visually hide content (and make it available only for screen readers)?
- [ ] Have you ever used a grid system, and if so, what do you prefer?
- [ ] Have you used or implemented media queries or mobile specific layouts/CSS?
- [ ] Are you familiar with styling SVG?
- [ ] How do you optimize your webpages for print?
- [ ] What are some of the "gotchas" for writing efficient CSS?
- [ ] What are the advantages/disadvantages of using CSS preprocessors?
  - [ ] Describe what you like and dislike about the CSS preprocessors you have used.
- [ ] How would you implement a web design comp that uses non-standard fonts?
- [ ] Explain how a browser determines what elements match a CSS selector.
- [ ] Describe pseudo-elements and discuss what they are used for.
- [ ] Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
- [ ] What does ```* { box-sizing: border-box; }``` do? What are its advantages?
- [ ] List as many values for the display property that you can remember.
- [ ] What's the difference between inline and inline-block?
- [ ] What's the difference between a relative, fixed, absolute and statically positioned element?
- [ ] The 'C' in CSS stands for Cascading. How is priority determined in assigning styles (a few examples)? How can you use this system to your advantage?
- [ ] What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
- [ ] Have you played around with the new CSS Flexbox or Grid specs?
- [ ] How is responsive design different from adaptive design?
- [ ] Have you ever worked with retina graphics? If so, when and what techniques did you use?
- [ ] Is there any reason you'd want to use ```translate()``` instead of absolute positioning, or vice-versa? And why?
- [ ] What are pseudo classes and what are they used for?
- [ ] Explain the three main ways to apply CSS styles to a Web page
- [ ] What is grouping and what is it used for?
- [ ] How to restore the default property value using CSS?
- [ ] What are the advantages and disadvantages of External Style Sheets?
- [ ] Explain the difference between ```visibility:hidden``` and ```display:none```

## JavaScript

- [ ] Explain event delegation
- [ ] Explain how ```this``` works in JavaScript
- [ ] Explain how prototypal inheritance works
- [ ] What do you think of AMD vs CommonJS?
- [ ] Explain why the following doesn't work as an IIFE: ```function foo(){ }();```.
  - [ ] What needs to be changed to properly make it an IIFE?
- [ ] What's the difference between a variable that is: ```null```, ```undefined``` or undeclared?
  - [ ] How would you go about checking for any of these states?
- [ ] What is a closure, and how/why would you use one?
- [ ] What's a typical use case for anonymous functions?
- [ ] How do you organize your code? (module pattern, classical inheritance?)
- [ ] What's the difference between host objects and native objects?
- [ ] Difference between: ```function Person(){}, var person = Person()```, and ```var person = new Person()```?
- [ ] What's the difference between ```.call``` and ```.apply```?
- [ ] Explain ```Function.prototype.bind```.
- [ ] When would you use ```document.write()```?
- [ ] What's the difference between feature detection, feature inference, and using the UA string?
- [ ] Explain Ajax in as much detail as possible.
- [ ] What are the advantages and disadvantages of using Ajax?
- [ ] Explain how JSONP works (and how it's not really Ajax).
- [ ] Have you ever used JavaScript templating?
  - [ ] If so, what libraries have you used?
- [ ] Explain "hoisting".
- [ ] Describe event bubbling.
- [ ] What's the difference between an "attribute" and a "property"?
- [ ] Why is extending built-in JavaScript objects not a good idea?
- [ ] Difference between document load event and document DOMContentLoaded event?
- [ ] What is the difference between ```==``` and ```===```?
- [ ] Explain the same-origin policy with regards to JavaScript.
- [ ] Make this work:
```js
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
- [ ] Why is it called a Ternary expression, what does the word "Ternary" indicate?
- [ ] What is ```"use strict";```? what are the advantages and disadvantages to using it?
- [ ] Create a for loop that iterates up to ```100``` while outputting "fizz" at multiples of ```3```, "buzz" at multiples of ```5``` and "fizzbuzz" at multiples of ```3``` and ```5```
- [ ] Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
- [ ] Why would you use something like the ```load``` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
- [ ] Explain what a single page app is and how to make one SEO-friendly.
- [ ] What is the extent of your experience with Promises and/or their polyfills?
- [ ] What are the pros and cons of using Promises instead of callbacks?
- [ ] What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
- [ ] What tools and techniques do you use debugging JavaScript code?
- [ ] What language constructions do you use for iterating over object properties and array items?
- [ ] Explain the difference between mutable and immutable objects.
  - [ ] What is an example of an immutable object in JavaScript?
  - [ ] What are the pros and cons of immutability?
  - [ ] How can you achieve immutability in your own code?
- [ ] Explain the difference between synchronous and asynchronous functions.
- [ ] What is event loop?
  - [ ] What is the difference between call stack and task queue?
- [ ] Explain the differences on the usage of ```foo``` between ```function foo() {}``` and ```var foo = function() {}```
- [ ] Can you name two programming paradigms important for JavaScript app developers?
- [ ] What is functional programming?
- [ ] What is the difference between classical inheritance and prototypal inheritance?
- [ ] What are the pros and cons of functional programming vs object-oriented programming?
- [ ] When is classical inheritance an appropriate choice?
- [ ] When is prototypal inheritance an appropriate choice?
- [ ] What does “favor object composition over class inheritance” mean?
- [ ] What are two-way data binding and one-way data flow, and how are they different?
- [ ] What are the pros and cons of monolithic vs microservice architectures?
- [ ] What is asynchronous programming, and why is it important in JavaScript?
- [ ] How do you check if an object is an array or not?
- [ ] Describe the different ways of creating objects and the ramifications of each. Provide examples.
- [ ] What is the significance of, and reason for, wrapping the entire content of a JavaScript source file in a function block?
- [ ] What is a potential pitfall with using ```typeof bar === "object"``` to determine if bar is an object? How can this pitfall be avoided?
- [ ] What will the code below output to the console and why?
```js
(function(){
  var a = b = 3;
})();

console.log("a defined? " + (typeof a !== 'undefined'));
console.log("b defined? " + (typeof b !== 'undefined'));
```
- [ ] What is ```NaN```? What is its type? How can you reliably test if a value is equal to NaN?
- [ ] Discuss possible ways to write a function ```isInteger(x)``` that determines if ```x``` is an integer.

## Testing

- [ ] What are some advantages/disadvantages to testing your code?
- [ ] What tools would you use to test your code's functionality?
- [ ] What is the difference between a unit test and a functional/integration test?
- [ ] What is the purpose of a code style linting tool?

## Performance

- [ ] What tools would you use to find a performance bug in your code?
- [ ] What are some ways you may improve your website's scrolling performance?
- [ ] Explain the difference between layout, painting and compositing.

## Network

- [ ] Traditionally, why has it been better to serve site assets from multiple domains?
- [ ] Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.
- [ ] What are the differences between Long-Polling, Websockets and Server-Sent Events?
- [ ] Explain the following request and response headers:
  - [ ] Diff. between Expires, Date, Age and If-Modified-...
  - [ ] Do Not Track
  - [ ] Cache-Control
  - [ ] Transfer-Encoding
  - [ ] ETag
  - [ ] X-Frame-Options
- [ ] What are HTTP methods? List all HTTP methods that you know, and explain them.
