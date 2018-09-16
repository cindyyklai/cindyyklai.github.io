---
id: 571
title: 'Javascript&#8217;s Reduce method'
date: 2017-12-31T20:04:38+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=571
permalink: /index.php/2017/12/31/javascripts-reduce-method/
categories:
  - Javascript
  - Programming
  - Technology
  - Web technologies
tags:
  - javascript
---
The Reduce method reduces an array into a single value by applying a callback function to each element in the array, starting with the leftmost to the rightmost element.

As a simple example, we could use reduce() to find the sum of all the numbers in an array.

<pre class="brush: plain; title: ; notranslate" title="">const numbers = [3, 2, 5, 7, 8, 10];
const sum = numbers.reduce(function (total, item) {
  return total + item;
});
// Returns 35
</pre>

In ES6 syntax,

<pre class="brush: plain; title: ; notranslate" title="">const numbers = [3, 2, 5, 7, 8, 10];
const sum = numbers.reduce((total, item) =&gt; total + item);
// Returns 35
</pre>

More great examples of the Reduce method:
  
https://medium.freecodecamp.org/reduce-f47a7da511a9

Full documentation:
  
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce