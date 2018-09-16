---
id: 240
title: Deleting multiple git branches
date: 2016-06-02T16:38:01+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=240
permalink: /index.php/2016/06/02/deleting-multiple-git-branches/
categories:
  - Git
  - Technology
  - Web technologies
---
Here&#8217;s something new I learned today. I was trying to clean up some stale branches but Tower only deletes one at a time even if you selected multiple of them! Well, that&#8217;s annoying. So I started searching on the internet and this seems to work:

  1. List all the branches that have the &#8216;PREFIX&#8217; prefix. This is just to preview the list before deleting it. <pre class="brush: plain; title: ; notranslate" title="">$ git branch -r | awk -F/ '/\/PREFIX/{print $2}'</pre>
    
    Note: -r shows all the remote branches. -a shows both local and remote.</li> 
    
      * If it looks good, delete away! (Scroll to see the command as it is pretty long) <pre class="brush: plain; title: ; notranslate" title="">$ git branch -r | awk -F/ '/\/PREFIX/{print $2}' | xargs -I {} git push origin :{}</pre>
        
        Note: As of Git v1.5.0, you can also delete a remote branch using:
        
        <pre class="brush: plain; title: ; notranslate" title="">$ git push origin --delete &lt;branchname&gt;</pre>
    
      * Remove local reference to those remote branches. <pre class="brush: plain; title: ; notranslate" title="">$ git remote prune origin</pre>
        
        or
        
        <pre class="brush: plain; title: ; notranslate" title="">$ git branch -D &lt;branch1&gt; &lt;branch2&gt; &lt;branch3&gt; </pre></ol>