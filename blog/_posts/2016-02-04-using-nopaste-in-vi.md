---
id: 199
title: 'Using &#8216;nopaste&#8217; in vi'
date: 2016-02-04T23:47:43+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=199
permalink: /index.php/2016/02/04/using-nopaste-in-vi/
categories:
  - Programming
  - Technology
---
To turn off autoindent when you paste code, there&#8217;s a special &#8220;paste&#8221; mode.
  
Type

<pre class="brush: plain; title: ; notranslate" title="">:set paste
</pre>

Then paste your code. Note that the text in the tooltip now says &#8212; INSERT (paste) &#8211;.
  
After you pasted your code, turn off the paste-mode, so that auto-indenting when you type works correctly again.

<pre class="brush: plain; title: ; notranslate" title="">:set nopaste
</pre>