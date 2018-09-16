---
id: 510
title: Installing Apache Maven on El Capitan
date: 2016-09-28T22:31:47+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=510
permalink: /index.php/2016/09/28/installing-apache-maven-on-el-capitan/
categories:
  - Apache
  - Maven
  - Programming
  - Technology
  - Web technologies
---
  * Add the following line to ~/.profile or ~/.bash_profile:

<pre class="brush: plain; title: ; notranslate" title="">export JAVA_HOME=$(/usr/libexec/java_home)</pre>

To verify the JAVA_HOME environment variable has been set correctly, type:

<pre class="brush: plain; title: ; notranslate" title="">echo $JAVA_HOME</pre>

which should return something like this:

<pre class="brush: plain; title: ; notranslate" title="">/Library/Java/JavaVirtualMachines/jdk1.8.0_102.jdk/Contents/Home</pre>

  * Verify that JDK 7+ is installed.  Type the following in a terminal window:

<pre class="brush: plain; title: ; notranslate" title="">java -version</pre>

It should give you something like this:

<pre class="brush: plain; title: ; notranslate" title="">java version "1.8.0_102"

Java(TM) SE Runtime Environment (build 1.8.0_102-b14)

Java HotSpot(TM) 64-Bit Server VM (build 25.102-b14, mixed mode)

</pre>

  * Download [Apache Maven 3.x Binaries](http://maven.apache.org/download.cgi)

(At the time this was written, the version was 3.3.9)

  * Extract the Maven Archive
  * Type the following lines in terminal:

<pre class="brush: plain; title: ; notranslate" title="">sudo su

mv [apache-maven-directory]/apache-maven-3.3.9 ~/opt

exit
</pre>

&nbsp;

where [apache-maven-directory] is the path of the directory where you extract the maven archive in.

  * Add Maven binaries to user path.  Add the following line in ~/.bash_profile

<pre class="brush: plain; title: ; notranslate" title="">export PATH=/opt/apache-maven-3.3.9/bin:$PATH

</pre>

save and quit the file, then execute .bash_profile again.

  * Verify Maven installation by typing:

<pre class="brush: plain; title: ; notranslate" title="">mvn -version</pre>

which should return something like this:

<pre class="brush: plain; title: ; notranslate" title="">Apache Maven 3.3.9 (bb52d8502b132ec0a5a3f4c09453c07478323dc5; 2015-11-10T08:41:47-08:00)

Maven home: /opt/apache-maven-3.3.9

Java version: 1.8.0_102, vendor: Oracle Corporation

Java home: /Library/Java/JavaVirtualMachines/jdk1.8.0_102.jdk/Contents/Home/jre

Default locale: en_US, platform encoding: UTF-8

OS name: "mac os x", version: "10.11.6", arch: "x86_64", family: "mac"

</pre>