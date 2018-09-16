---
id: 11
title: Finding a bad commit with git-bisect
date: 2015-10-05T16:47:11+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=11
permalink: /index.php/2015/10/05/finding-a-bad-commit-with-git-bisect/
categories:
  - Git
  - Technology
tags:
  - git
---
When working on a project last year, I was introduced to this handy feature in Git &#8211; git bisect.  According to https://git-scm.com/docs/git-bisect, it allows you to:

> Use binary search to find the commit that introduced a bug

It is pretty straightforward to use it:

  1. Initiate a bisect session 
    <pre>$ git bisect start</pre>

  2. Specify a good commit 
    <pre>$ git bisect good d89ec</pre>

  3. Specify a bad commit 
    <pre>$ git bisect bad 96cac</pre>

  4. At this point, Git will output something like this: 
    <pre>Bisecting: 6 revisions left to test after this (roughly 3 steps)</pre>

  5. Test your site, if it looks good, type: 
    <pre>$ git bisect good</pre>
    
    Otherwise,
    
    <pre>$ git bisect good</pre>

  6. Now git will output something like:Bisecting: 3 revisions left to test after this (roughly 2 steps)
  7. Repeat Step 5 until there&#8217;s git says something like this:d89ecffb672c142cadbbaeef5e31597aac6ecf06 is the first bad commit

&nbsp;