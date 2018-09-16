---
id: 215
title: What is Composer?
date: 2016-03-11T00:06:45+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=215
permalink: /index.php/2016/03/11/what-is-composer/
categories:
  - PHP
  - Technology
  - Web technologies
---
Summarized from this [article](https://semaphoreci.com/community/tutorials/getting-started-with-composer-for-php-dependency-management):
  
&#8211; PEAR installs dependencies globally and Composer installs them locally, in your project structure.
  
&#8211; PEAR is essentially a package manager and Composer is a dependency manager.

To install Composer, run:

<pre class="brush: plain; title: ; notranslate" title="">curl -sS https://getcomposer.org/installer | php
</pre>

To configure Composer:
  
&#8211; Create a file named composer.json in project root.
  
&#8211; Add dependencies to composer.json like this:

<pre class="brush: plain; title: ; notranslate" title="">{
  "require": {
    "php": "&gt;5.4.2",
    "other_dependency": "~1.0"
  }
}
</pre>

To install dependencies as specified in composer.json:

<pre class="brush: plain; title: ; notranslate" title="">php composer.phar install -v
</pre>

To update dependencies:

<pre class="brush: plain; title: ; notranslate" title="">php composer.phar update
</pre>

To update a single library:

<pre class="brush: plain; title: ; notranslate" title="">composer.phar update doctrine/doctrine-fixtures-bundle
</pre>