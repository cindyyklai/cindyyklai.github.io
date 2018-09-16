---
id: 54
title: 'Neat trick on CSS&#8217;s :before and :after pseudo elements'
date: 2015-11-06T22:10:37+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=54
permalink: /index.php/2015/11/06/interesting-observation-on-csss-before-and-after/
categories:
  - CSS
  - Technology
tags:
  - css
---
Suppose we have these HTML elements:

<pre class="brush: plain; title: ; notranslate" title="">&lt;div class="element1"&gt;Element1&lt;/div&gt;
&lt;div class="element2"&gt;Element2&lt;/div&gt;
</pre>

And suppose this is the CSS:

<pre class="brush: plain; title: ; notranslate" title="">.element1, .element2 {
    display: inline;
}
.element1:before {
    content: '#';
  }
.element2:after {
    content: '#';
  }
</pre>

We can expect to see two #&#8217;s between element1 and element2.

Now, change the #&#8217;s to spaces.

<pre class="brush: plain; title: ; notranslate" title="">.element1, .element2 {
    display: inline;
}
.element1:before {
    content: ' ';
  }
.element2:after {
    content: ' ';
  }
</pre>

Surprisingly, it only inserts one space between the elements. This can be handy when trying to ensure that there&#8217;s always a space between two elements. If one of this elements is not present, then the space is omitted. If you want to enforce two blank spaces between them, use &#8216;\00a0&#8217;.

<pre class="brush: plain; title: ; notranslate" title="">.element1, .element2 {
    display: inline;
}
.element2:before {
    content: '&#92;&#48;0a0';
  }

  .element1:after {
    content: '&#92;&#48;0a0';
  }
</pre>