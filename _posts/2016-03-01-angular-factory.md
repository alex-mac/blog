---
layout: post
title: Angular Factories
date:   2016-03-01 23:45:41 -0800
---

Angular has a lot of services available that may be confusing at first especially for new devs. One of which is the Factory service. the [Angular documentation](https://docs.angularjs.org/guide/services) provides the following definition 
for what a service is: 

> The service factory function generates the single object or function that represents the service to the rest of the application. The object or function returned by the service is injected into any component (controller, service, filter or directive) that specifies a dependency on the service.

What does this mean? Lets break it down! 

A factory in angular:

* generates an object or a function
* this object or function can be used throughout the app 
* access to this object or function is done via injection into any component

So, basically, a factory in Angular allows code (whether it be an object that you need to pass throughout the app or functions relavent to particular components) to be made into components to be reused rather than hardcoding the same logic into controllers. Inject is a scary word, but think of it as just that: you're injecting (or inserting) your code that you created in your factory into a controller, a service, or a directive. 

One instance of a factory i've encountered is to use it to pass data along an app. Say you have a form and your client wants you to create multiple pages to help make the flow of the form better and more dynamic. You can use a factory to create an object that contains all of the information the user has filled out and submit the data in one go at the very end. 

{% highlight javascript %}
  var myModule = angular.module('myModule', []);
myModule.factory('serviceId', function() {
  var shinyNewServiceInstance;
  // factory function body that constructs shinyNewServiceInstance
  return shinyNewServiceInstance;
});
{% endhighlight %}

