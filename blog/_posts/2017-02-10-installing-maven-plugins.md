---
id: 534
title: Installing Maven plugins
date: 2017-02-10T22:42:42+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=534
permalink: /index.php/2017/02/10/installing-maven-plugins/
categories:
  - Apache
  - Maven
  - Programming
  - Technology
  - Web technologies
---
To download plugins and the required dependencies, run this command:

<pre class="brush: plain; title: ; notranslate" title="">mvn org.apache.maven.plugins:maven-dependency-plugin:2.6:get -Dartifact=groupId:artifactId:version</pre>

For example, to download versions-maven-plugin:

<pre class="brush: plain; title: ; notranslate" title="">mvn org.apache.maven.plugins:maven-dependency-plugin:2.6:get -Dartifact=org.codehaus.mojo:versions-maven-plugin:2.3 -DrepoUrl=https://github.com/mojohaus/versions-maven-plugin</pre>

If the plugins need to be installed manually, refer to [this documentation on the Apache Maven project site](http://maven.apache.org/plugins/maven-install-plugin/examples/custom-pom-installation.html).