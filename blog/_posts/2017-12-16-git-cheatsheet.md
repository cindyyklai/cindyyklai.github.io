---
id: 556
title: Git cheatsheet
date: 2017-12-16T16:45:13+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=556
permalink: /index.php/2017/12/16/git-cheatsheet/
categories:
  - Programming
  - Technology
tags:
  - git
---
See all local branches

<pre class="brush: plain; title: ; notranslate" title="">git branch
</pre>

See all remote branches

<pre class="brush: plain; title: ; notranslate" title="">git branch -r
</pre>

See all branches

<pre class="brush: plain; title: ; notranslate" title="">git branch -a
</pre>

Clone a git repo

<pre class="brush: plain; title: ; notranslate" title="">git clone [url]
</pre>

Create a local branch from remote and switch to it

<pre class="brush: plain; title: ; notranslate" title="">git checkout -b &lt;branch&gt; &lt;remote&gt;/&lt;branch&gt;
</pre>

List the current configured remote repository for your fork.

<pre class="brush: plain; title: ; notranslate" title="">git remote -v
</pre>

List recent commits

<pre class="brush: plain; title: ; notranslate" title="">git log
</pre>

Add a new remote upstream repository

<pre class="brush: plain; title: ; notranslate" title="">git remote add upstream [url]
</pre>

See what files are changed

<pre class="brush: plain; title: ; notranslate" title="">git status
</pre>

See only changes that have already been added to the Staging Area

<pre class="brush: plain; title: ; notranslate" title="">git diff --staged
</pre>

Show unstaged changes

<pre class="brush: plain; title: ; notranslate" title="">git diff
</pre>

Push to remote

<pre class="brush: plain; title: ; notranslate" title="">git push &lt;remote&gt; &lt;branch&gt;
</pre>

Check out pull requests locally

In .git/config add this under the [remote &#8220;upstream&#8221;] section

<pre class="brush: plain; title: ; notranslate" title="">fetch = +refs/pull/*/head:refs/remotes/origin/pr/*:
</pre>

To check out a particular pull request:

<pre class="brush: plain; title: ; notranslate" title="">git checkout pr/999
</pre>

Excellent Git resources
  
https://services.github.com/on-demand/downloads/github-git-cheat-sheet/
  
https://www.git-tower.com/learn/git/ebook/en/command-line/introduction#start