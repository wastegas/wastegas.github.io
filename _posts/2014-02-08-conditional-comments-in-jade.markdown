---
layout: post
title: "Conditional comments in Jade"
date: 2014-02-08 08:26:10
categories: html conditional comments jade express
---

After doing a lot of searching on how to do conditional formatting in [Jade](http://jade-lang.com/), this format worked for me.

{% highlight html %}
    <!--[if lt IE 9]> 
    <script src="https://oss.maxcdn.com/libs/html5shiv/3.7.0/html5shiv.js"></script>
    <script src="https://oss.maxcdn.com/libs/respond.js/1.4.2/respond.min.js"></script>
    <![endif]-->
{% endhighlight %}

Note the script tags are not indented. This will prevent parsing errors in [Express](http://expressjs.com/) complaining about unexpected indent.
