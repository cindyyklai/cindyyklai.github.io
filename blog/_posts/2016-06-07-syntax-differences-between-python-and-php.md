---
id: 253
title: Syntax differences between Python and PHP
date: 2016-06-07T23:08:53+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=253
permalink: /index.php/2016/06/07/syntax-differences-between-python-and-php/
categories:
  - PHP
  - Programming
  - Python
  - Technology
---
As a PHP developer for over ten years, I can&#8217;t help by compare its syntax with Python when I started learning the latter recently. I anticipate this page will be a perpetual work in progress&#8230;

## Variable names

PHP &#8211; &#8216;$&#8217; in front of variable names.  E.g.,

<pre class="brush: plain; title: ; notranslate" title="">$str = 'abc';</pre>

Python &#8211; No &#8216;$&#8217; in front of variable names.  E.g.,

<pre class="brush: plain; title: ; notranslate" title="">str = 'abc'</pre>

&nbsp;

## Semicolons

PHP &#8211; Must have a semicolon to end each line of code. E.g.,

<pre class="brush: plain; title: ; notranslate" title="">$str = 'abc';&lt;/pre&gt;
&lt;pre&gt;$str2 = 'def';&lt;/pre&gt;
&lt;pre&gt;</pre>

Python &#8211; Each line must be ended with a newline.  E.g.,

<pre class="brush: plain; title: ; notranslate" title="">str = 'abc'
str2 = 'def'</pre>

&nbsp;

## &#8216;If&#8217; statements

PHP

<pre class="brush: plain; title: ; notranslate" title="">if ($city == "Charlotte"):
  return 183;
elseif ($city == "Tampa"):
  return 220;
else:
  return 475;
endif;
</pre>

Python

&#8211; IMPORTANT: The indent must be 4 spaces.

<pre class="brush: plain; title: ; notranslate" title="">if city == "Charlotte":
        return 183
    elif city == "Tampa":
        return 220
    else:
        return 475
</pre>

&nbsp;

## Functions

PHP

<pre class="brush: plain; title: ; notranslate" title="">function render($arg = NULL) {
}
</pre>

Python

<pre class="brush: plain; title: ; notranslate" title="">def render(arg):
</pre>

## Arrays in PHP = Lists in Python

PHP

<pre class="brush: plain; title: ; notranslate" title="">$array = ['a', 2, 'c'];</pre>

Python

<pre class="brush: plain; title: ; notranslate" title="">array = ['a', 2, 'c']</pre>

## Associative arrays in PHP = Dictionaries in Python

PHP

<pre class="brush: plain; title: ; notranslate" title="">$array = [
    "foo" =&gt; "bar",
    "bar" =&gt; ['flint', 'twine', 'gemstone'],
];
</pre>

Python (Syntax is very similar to JSON)

<pre class="brush: plain; title: ; notranslate" title="">array = {
    'foo' : 'bar',
    'bar' : ['flint', 'twine', 'gemstone']
}
</pre>

## For loop

PHP

<pre class="brush: plain; title: ; notranslate" title="">foreach ($arr as $value) {
}
</pre>

Python

<pre class="brush: plain; title: ; notranslate" title="">for value in arr:
</pre>

## PHP&#8217;s implode = Python&#8217;s join

PHP

<pre class="brush: plain; title: ; notranslate" title="">$s = "-";
$seq = ("a", "b", "c"); # This is sequence of strings.
print implode($s, $seq); # Will print a-b-c
</pre>

Python

<pre class="brush: plain; title: ; notranslate" title="">s = "-"
seq = ("a", "b", "c") # This is sequence of strings.
print s.join( seq ) # Will print a-b-c
</pre>

## & operator</h2 [source] PHP - Uses double & Python - Uses single & [/source] 

## Constructors

PHP

<pre class="brush: plain; title: ; notranslate" title="">function __construct()</pre>

Python

<pre class="brush: plain; title: ; notranslate" title="">def __init__(self)</pre>

Inheritance
  
PHP

<pre class="brush: plain; title: ; notranslate" title="">class Bar extends Foo</pre>

Python

<pre class="brush: plain; title: ; notranslate" title="">class Bar(Foo)</pre>

Parent class
  
PHP

<pre class="brush: plain; title: ; notranslate" title="">parent::foo()</pre>

Python
  
super(bar(), self).foo()