---
id: 212
title: Drush not able to connect to database in MAMP
date: 2016-02-18T18:41:24+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=212
permalink: /index.php/2016/02/18/drush-not-able-to-connect-to-database-in-mamp/
categories:
  - Drupal
  - Technology
---
Recently I was helping a coworker to set up his drush and we ran into this problem:

<pre class="brush: plain; title: ; notranslate" title="">Drush was not able to start (bootstrap) the Drupal [error]
database.
</pre>

After hours of troubleshooting, I added these lines to his .bash_profile, as suggested by this this post:

<pre class="brush: plain; title: ; notranslate" title="">export PATH="/Applications/MAMP/Library/bin:/Applications/MAMP/bin/php5.5.10/bin:$PATH"

export PATH
export DRUSH_PHP="/Applications/MAMP/bin/php/php5.5.10/bin/php"
export PATH=/usr/local/bin:$PATH
</pre>

And voila, it&#8217;s working!