---
id: 26
title: Pass parameters to MySQL script from Shell
date: 2015-11-04T23:29:28+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=26
permalink: /index.php/2015/11/04/pass-parameters-to-mysql-script-from-shell/
categories:
  - MySQL
  - Programming
  - Technology
---
If you would like to make your MySQL script dynamic and flexible by passing parameters to it, here&#8217;s what I learned recently.

Suppose this is your MySQL script

<pre class="brush: csharp; title: ; notranslate" title="">SELECT *
FROM table1
WHERE date_modified &gt;= @start_date AND date_modified &lt;= @end_date
</pre>

In your Shell script,

<pre class="brush: csharp; title: ; notranslate" title="">#!/bin/bash -l

# Make sure that user supplies the parameters
if [ $# -ne "$ARGS" ]
then
        echo "You passed $# parameters"
        echo "Usage: `basename $0` sql_file_name start_date end_date"
exit
fi

# Execute the MySQL script with the parameters
mysql -uroot -ppassword –h mysql-host -e "set @start_date:='$2'; set @end_date:='$3'; source $1;"
</pre>