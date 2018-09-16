---
id: 475
title: What are PHP traits?
date: 2016-08-19T16:36:28+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=475
permalink: /index.php/2016/08/19/what-are-php-traits/
categories:
  - PHP
  - Programming
tags:
  - php
---
Traits are a group of functions that can be included in other classes. For example,

<pre class="brush: plain; title: ; notranslate" title="">trait A {
    public function test() {
        print 'HELLO';
    }
}

class B {
    use A;
}

class C {
    use A;
}

$b = new B();
$b-&gt;test(); // Will print 'Hello'.

$c = new C();
$c-&gt;test(); // Will print 'Hello'.
</pre>