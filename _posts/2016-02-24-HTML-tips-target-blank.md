---
layout: post
title: HTML Tips Target Blank
date:   2016-02-09 23:45:41 -0800
---

Right now, I'm currently doing some freelancing at a dev shop and one of my awesome coworkers mentioned something so quickly and succinctly that blew my mind away that I wanted to share with you guys. If you ever wondered about how to manipulate links to other websites, this subtle difference can make a huge world of difference in terms of UX/UI. 

As of right now, if you were to use a regular a tag ```<a href="http://not-my-website.com"></a>```, this syntax would send you to that website after you click it in the same tag. To open the link in a new tag, make sure to use ```target="_blank"```. This will open that link in a new tab rather then the same tag. This is useful for pages such as your portfolio so that people checking out your projects can go back to your portfolio page more easily without having to hit back several times. 

example of the implimentation

{% highlight html %}
  <a href="http://google.com" target="_blank">Click me to go to google</a>
{% endhighlight %}