---
id: 637
title: Setting up Jekyll for Github Pages
date: 2018-09-13T00:46:36+00:00
author: cindylai
layout: post
guid: http://cindylai.net/?p=637
permalink: /index.php/2018/09/13/setting-up-jekyll-for-using-github-pages/
categories:
  - Uncategorized
---
So, I have been using WordPress as my personal blogging tool. I don&#8217;t need any fancy stuff or lots of customizations for my site as all I would like to do is to document what I&#8217;ve learned and share with others. In this aspect, an out-of-the-box WordPress site with a few plugins works great for me. However, when I heard about GitHub Pages, I couldn&#8217;t wait to try it. Why? Because it is free. Take a look at this bill from my hosting company this year:

<img src="http://cindylai.net/wp-content/uploads/2018/09/21_days_left_until_service_expiration_-_cindy_yk_lai_gmail_com_-_Gmail.png" alt="" width="616" height="269" class="aligncenter size-full wp-image-658" srcset="http://cindylai.net/wp-content/uploads/2018/09/21_days_left_until_service_expiration_-_cindy_yk_lai_gmail_com_-_Gmail.png 616w, http://cindylai.net/wp-content/uploads/2018/09/21_days_left_until_service_expiration_-_cindy_yk_lai_gmail_com_-_Gmail-300x131.png 300w" sizes="(max-width: 616px) 100vw, 616px" />

To most people, $143 is not a lot of money. However, I can&#8217;t justify spending over $100 on a very basic site every year when there is a free alternative. Moreover, this fee goes up every year! Look at how much it was last year:

<img src="http://cindylai.net/wp-content/uploads/2018/09/7_days_left_until_service_expiration_-_cindy_yk_lai_gmail_com_-_Gmail.png" alt="" width="612" height="329" class="aligncenter size-full wp-image-659" srcset="http://cindylai.net/wp-content/uploads/2018/09/7_days_left_until_service_expiration_-_cindy_yk_lai_gmail_com_-_Gmail.png 612w, http://cindylai.net/wp-content/uploads/2018/09/7_days_left_until_service_expiration_-_cindy_yk_lai_gmail_com_-_Gmail-300x161.png 300w" sizes="(max-width: 612px) 100vw, 612px" />

While I will pay to keep my domain, it doesn&#8217;t make sense for me to continue with the hosting service. I am motivated/determined to get my WordPress site migrated to GitHub before the hosting service expires!

I&#8217;ve also decided to document my journey of setting up Jekyll and using it as a blogging tool on my GitHub site. So here you go!

# Prerequisites &#8211; Ruby and Jekyll

Per the [Jekyll official website](https://jekyllrb.com/docs/installation/), Jekyll requires Ruby version 2.2.5 or above.

I had to update my Ruby as the version shipped with my Mac OS definitely did not meet this requirement.

<pre>[515] cindylai@MacBook-Pro-201 - 03:28:10 $ ruby -v
ruby 2.2.2p95 (2015-04-13 revision 50295) [x86_64-darwin14]</pre>

So, I tried:

<pre>rvm install ruby-2.5.1</pre>

And got this message:

<pre>Warning! PATH is not properly set up, /Users/cindylai/.rvm/gems/ruby-2.2.2/bin is not at first place.
         Usually this is caused by shell initialization files. Search for PATH=... entries.
         You can also re-add RVM to your profile by running: rvm get stable --auto-dotfiles
         To fix it temporarily in this shell session run: rvm use ruby-2.2.2
         To ignore this error add rvm_silence_path_mismatch_check_flag=1 to your ~/.rvmrc file.
Already installed ruby-2.5.1.
To reinstall use:

    rvm reinstall ruby-2.5.1
</pre>

Well, at least there are instructions on how to fix it. To reload RVM, simply do:

<pre>rvm get stable --auto-dotfiles</pre>

And now, the following confirms that I&#8217;m on the latest version:

<pre>[525] cindylai@MacBook-Pro-201 - 03:33:46 $ ruby -v
ruby 2.5.1p57 (2018-03-29 revision 63029) [x86_64-darwin17]</pre>

I then proceeded to install Jekyll and bundler gems:

<pre>gem install jekyll bundler</pre>

# Creating a new Jekyll site

At this point, I thought I was done with all the set up and ready to create my Jekyll site, so I did:

<pre>jekyll new myblog</pre>

And of course, it didn&#8217;t go as planned. This is what it returned:

<pre>/Users/cindylai/.rvm/gems/ruby-2.5.1/gems/bundler-1.16.4/lib/bundler/resolver.rb:285:in `block in verify_gemfile_dependencies_are_found!': Could not find gem 'github-pages' in any of the gem sources listed in your Gemfile. (Bundler::GemNotFound)

</pre>

This time Ruby didn&#8217;t tell me how to fix it, but I found a [helpful answer](https://blog.mattclemente.com/2016/02/24/getting-started-with-jekyll-part-3.html) , which is to run:

<pre>bundle install</pre>

After that, Ruby successfully installed Jekyll and other dependencies from the GitHub Pages gem.

Now, I ran

<pre>jekyll new myblog</pre>

again and this time it worked.

<img class="aligncenter size-large wp-image-649" src="http://cindylai.net/wp-content/uploads/2018/09/myblog-1024x264.png" alt="" width="600" height="155" srcset="http://cindylai.net/wp-content/uploads/2018/09/myblog-1024x264.png 1024w, http://cindylai.net/wp-content/uploads/2018/09/myblog-300x77.png 300w, http://cindylai.net/wp-content/uploads/2018/09/myblog-768x198.png 768w, http://cindylai.net/wp-content/uploads/2018/09/myblog.png 1080w" sizes="(max-width: 600px) 100vw, 600px" />

Next, I ran:

<pre>bundle exec jekyll serve</pre>

Jekyll successfully served up my blog but there are a couple of warnings:

<pre>Configuration file: none
            Source: /Users/cindylai/Documents/Personal/github/cindyyklai.github.io
       Destination: /Users/cindylai/Documents/Personal/github/cindyyklai.github.io/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
     Build Warning: Layout 'post' requested in myblog/_posts/2018-09-12-welcome-to-jekyll.markdown does not exist.
   GitHub Metadata: No GitHub API authentication could be found. Some fields may be missing or have incorrect data.
     Build Warning: Layout 'page' requested in myblog/about.md does not exist.
     Build Warning: Layout 'home' requested in myblog/index.md does not exist.
                    done in 2.405 seconds.
 Auto-regeneration: enabled for '/Users/cindylai/Documents/Personal/github/cindyyklai.github.io'
    Server address: http://127.0.0.1:4000
  Server running... press ctrl-c to stop.

</pre>

Upon googling this issue, I stumbled across https://github.com/jekyll/jekyll/issues/6047. And based on one of the comments, this seems to be expected starting Jekyll 3.2. This is the statement on the [Jekyll official site](https://jekyllrb.com/docs/structure/):

<img src="http://cindylai.net/wp-content/uploads/2018/09/Directory_Structure___Jekyll_•_Simple__blog-aware__static_sites.png" alt="" width="733" height="245" class="aligncenter size-full wp-image-679" srcset="http://cindylai.net/wp-content/uploads/2018/09/Directory_Structure___Jekyll_•_Simple__blog-aware__static_sites.png 733w, http://cindylai.net/wp-content/uploads/2018/09/Directory_Structure___Jekyll_•_Simple__blog-aware__static_sites-300x100.png 300w" sizes="(max-width: 733px) 100vw, 733px" />

And I confirm that I&#8217;m on 3.7.4:

<pre>[536] cindylai@MacBook-Pro-201 - 08:54:44 $ jekyll -v
jekyll 3.7.4
</pre>