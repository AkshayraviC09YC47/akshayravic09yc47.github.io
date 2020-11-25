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
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~

And here is the same code with syntax highlighting:

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```

And here is the same code yet again but with line numbers:

{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}

## Boxes
You can add notification, warning and error boxes like this:

### Notification

{: .box-note}
**Note:** This is a notification box.

### Warning

{: .box-warning}
**Warning:** This is a warning box.

### Error

{: .box-error}
**Error:** This is an error box.
