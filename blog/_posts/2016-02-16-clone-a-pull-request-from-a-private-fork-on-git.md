---
id: 209
title: Clone a pull request from a private fork on Git
date: 2016-02-16T20:09:49+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=209
permalink: /index.php/2016/02/16/clone-a-pull-request-from-a-private-fork-on-git/
categories:
  - Git
  - Programming
  - Technology
---
Something I learned today:

To clone a pull request from a private fork, run these commands:

<pre class="brush: plain; title: ; notranslate" title="">git fetch origin pull/PR_ID/head:branch_name</pre>

<pre class="brush: plain; title: ; notranslate" title="">git checkout branch_name</pre>

Substitute PR\_ID with the pull request ID and branch\_name with the branch name.