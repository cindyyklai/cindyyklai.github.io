---
id: 195
title: Download webpage via wget
date: 2016-02-04T23:43:01+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=195
permalink: /index.php/2016/02/04/download-webpage-via-wget/
categories:
  - Programming
  - Technology
---
If you want to download a webpage and its dependencies, including css images, here&#8217;s a useful command:

<pre class="brush: plain; title: ; notranslate" title="">wget --page-requisites http://example.com/your/page.html
</pre>