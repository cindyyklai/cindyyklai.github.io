---
id: 227
title: 'NPM/Bower/Composer/Homebrew &#8211; What are the differences?'
date: 2016-05-19T22:05:12+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=227
permalink: /index.php/2016/05/19/npmbowercomposerhomebrew-what-are-the-differences/
categories:
  - Programming
  - Technology
  - Web technologies
---
For a while, I have been confused with all the different package managers that are floating around. NPM, Bower, Composer, Homebrew are some of the popular ones that I have used at work. So what are they and how do they differ from each other?

  * npm &#8211; Package manager for nodes. It comes with nodejs ([What exactly is nodejs?](http://cindylai.net/index.php/2016/02/04/what-exactly-is-node-js/)).
  * bower &#8211; Package manager for front-end web projects. It manages components that contain HTML, CSS, JavaScript, fonts or even image files. It is also an npm package (You will need npm and nodejs to install bower and to execute it. See [Getting started with Bower](http://cindylai.net/index.php/2015/11/05/getting-started-with-bower/).)
  * composer &#8211; Dependency manager for php projects (I have used this to install/update dependencies for Drupal sites)
  * Homebrew &#8211; Package manager for Mac OS X

And here is one of the ways how they cross paths with each other:
  
1) Install Homebrew (I use a Mac)
  
2) Use Homebrew to install node (It can also be downloaded from https://nodejs.org/en/, in that case &#8211; skip Step 1)
  
3) Install Bower with npm

`npm install -g bower`

4) Install jQuery with Bower
  
`bower install jquery`

Please note that Bower is not needed to install Javascript libraries &#8211; NPM can do the same. There are some articles on the web that talk about the drawbacks of using Bower:

  * https://gofore.com/stop-using-bower/
  * https://medium.com/@nickheiner/why-my-team-uses-npm-instead-of-bower-eecfe1b9afcb#.gm5edekzx