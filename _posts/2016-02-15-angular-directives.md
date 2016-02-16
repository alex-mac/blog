---
layout: post
title: Angular Directives
date: 2016-02-15 16:27:31 - 0800
---

Today we're going to talk about directives in Angular! I'll be using code from my portfolio to demonstrate. 

Directives in Angular are probably one of the most difficult concepts for me to pick up thus far. That being said, however, they are one of the most amazing features about Angular (alongside components in Angular 1.5.0).

What is a directive? The dictionary definition is "an official or authoritative instruction." Basically, it's something that provides instruction to inform others of its purpose. A directive in Angular is similar to html tags in ... well, HTML. The <h1> header tags in ```<h1>Hello World</h1>``` provide information for your browser with rules for interperating and displaying the content enclosed between the opening and closing tags. In Angular, you are not limited in what kind of "tags" you can use! You can create custom directives such as ```<card></card>``` or ```<book></book>``` or anything else you would like to categorize on your page.

This is an example of html code that was used to loop through an object and show its information on my projects page:

{% highlight html %}
<div id="cols" ng-repeat="project in projects" >
  <div >
  <a href="{% raw %}{{ project.link }}{% endraw %}">
    <div class = "proj-image" id="{% raw %}proj{{project.id}}{% endraw %}">
      <h1 class="centering" ng-class="{% raw %}{highlight: hover2}{% endraw %}" ng-mouseenter="hover2 = true" ng-mouseleave="hover2 = false">
        {% raw %}{{ project.title }}{% endraw %}
      </h1>
    </div>
  </a>
  <br/>
  <p align="center">Github Repo: <a href="{% raw %}{{project.github}}{% endraw %}"><i class="fa fa-github-alt"></i></a></p>
  <p class="content">
    {% raw %}{{project.content}}{% endraw %}
  </p>
</div>
{% endhighlight %}

As developers, we don't want this. We don't want someone to have to read through all this codee just to figure out what it's trying to do. That's where directives come in.  

{% highlight html %}
<div id="cols" ng-repeat="project in projects" >
  <div project-tile project="project"></div>
</div>
{% endhighlight %}

The second block of code is much cleaner and allows someone reading through your code to quickly assess what the code is doing (for anyone unfamiliar with Angular, within a div with the id of cols, repeat over every item in the array "projects" in our controller, and create a project-tile for each one).

That's it for now guys! I'll be adding an implimentation walkthrough of it at a later time !