---
id: 14
title: Redirect http to https
date: 2015-10-05T16:53:05+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=14
permalink: /index.php/2015/10/05/redirect-http-to-https/
categories:
  - Apache
  - Technology
---
RewriteEngine On

RewriteCond %{HTTPS} off

RewriteRule `<span class="pun">^(.*)</span><span class="pln">$ https</span><span class="pun">:</span><span class="com">//%{SERVER_NAME}%{REQUEST_URI} [L,R]</span>`