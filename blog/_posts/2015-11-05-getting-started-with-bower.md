---
id: 35
title: Getting started with Bower
date: 2015-11-05T18:03:49+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=35
permalink: /index.php/2015/11/05/getting-started-with-bower/
categories:
  - Technology
  - Web technologies
tags:
  - Bower
  - front-end
  - web development
---
If you&#8217;re new to Bower, [codementor](https://www.codementor.io/bower/tutorial/beginner-tutorial-getting-started-bower-package-manager) has a great beginners guide. It gives you an introduction of what Bower is and walks you through the installation process.

  1. Download node from [nodejs.org](https://nodejs.org/en/).
  2. Install Bower <pre class="brush: plain; title: ; notranslate" title="">sudo npm install -g bower</pre>
    
    Note: I tried running the command without sudo and got the following error, and after searching on the web, found that it needs to be run with root access or permissions to install Bower globally.
    
    <pre class="brush: plain; title: ; notranslate" title="">Please try running this command again as root/Administrator.</pre>

  3. As an example, use Bower to install jQuery. Navigate to your site root and run the following command:</p> <pre class="brush: plain; title: ; notranslate" title="">$ bower install jquery</pre>
    
    Note: To install a specific version, you can use
    
    <pre class="brush: plain; title: ; notranslate" title="">bower install bootstrap#version_number</pre>
    
    Here&#8217;s the output
  
    `<br />
? May bower anonymously report usage statistics to improve the tool over time? (Y/n) bower jquery#*              not-cached git://github.com/jquery/jquery.git#*<br />
bower jquery#*                 resolve git://github.com/jquery/jquery.git#*<br />
bower jquery#*                download https://github.com/jquery/jquery/archive/2.1.4.tar.gz<br />
bower jquery#*                 extract archive.tar.gz<br />
bower jquery#*                resolved git://github.com/jquery/jquery.git#2.1.4<br />
bower jquery#~2.1.4            install jquery#2.1.4</p>
<p>jquery#2.1.4 bower_components/jquery<br />
` 
    
    Bower installed the package into a newly created folder called &#8216;bower_components&#8217;.
  
    ![Bower components](http://cindylai.net/wp-content/uploads/2015/11/post_35_a.png)</li> 
    
      * To update the package, just run this command:</p> <pre class="brush: plain; title: ; notranslate" title="">$ bower update jquery</pre></ol> 
    
    That&#8217;s it! Of course, there&#8217;s more to it. There are some really useful tips and tricks in this [article at CSS-Tricks](https://css-tricks.com/whats-great-bower/) that I can&#8217;t wait to try. And the list of all the commands can be found on the [Bower API site](http://bower.io/docs/api/).