---
layout: post
title:  "Angular Directives"
date:   2016-02-15 216:35:19 -0800
categories: jekyll update
---

from 
{% highlight html %}
<div id="column">
  <div class="scroll">
    <div id="cols" ng-repeat="project in projects" >
      <div >
      <a href="{{ project.link }}">
        <div class = "proj-image" id="proj{{project.id}}">
          <h1 class="centering" ng-class="{highlight: hover2}" ng-mouseenter="hover2 = true" ng-mouseleave="hover2 = false">
            {{ project.title }}
          </h1>
        </div>
      </a>
      <br/>
        <p align="center">Github Repo: <a href="{{project.github}}"><i class="fa fa-github-alt"></i></a></p>
      <p class="content">
        {{project.content}}
      </p>
    </div>
  </div>
</div>
{% endhighlight %}}

To: 
{% highlight html %}
<div id="column">
  <div class="scroll">
    <div id="cols" ng-repeat="project in projects" >
      <div project-tile project="project"></div>
  </div>
</div>
{% endhighlight %}

