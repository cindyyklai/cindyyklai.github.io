---
id: 478
title: Installing Apache Maven on Mac
date: 2016-09-13T21:56:44+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=478
permalink: /index.php/2016/09/13/installing-apache-maven-on-mac/
categories:
  - Apache
  - Maven
  - Programming
  - Technology
  - Web technologies
---
While the [installation guide on Apache](https://maven.apache.org/install.html) is helpful, I decided to document the exact steps (some are not covered on the Apache site) I took to get Apache Maven installed in my machine.

  1. Add JAVA\_HOME environment variable to .bash\_profile</p> <pre class="brush: plain; title: ; notranslate" title="">export JAVA_HOME=$(/usr/libexec/java_home)</pre>

  2. Reload .bash_profile by running:</p> <pre class="brush: plain; title: ; notranslate" title="">. ~/.bash_profile</pre>

  3. Download the Apache Maven distribution archive from [here](https://maven.apache.org/download.cgi). 
  4. Add the bin directory to the PATH environment variable.
  
    In, .bashrc, add:</p> <pre class="brush: plain; title: ; notranslate" title="">export PATH=/path/to/apache/maven-3.3.9/bin:$PATH</pre>

  5. Reload .bashrc by running:</p> <pre class="brush: plain; title: ; notranslate" title="">. ~/bashrc</pre>

  6. Type the following the confirm Maven has been installed successfully:</p> <pre class="brush: plain; title: ; notranslate" title="">mvn -v</pre>