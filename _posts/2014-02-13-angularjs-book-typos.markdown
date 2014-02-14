---
layout: post
title: "Typos in O'Reilly AngularJS book"
date: 2014-02-13 21:25:00
categories: angularjs o'rielly book ng-route
---

I'm doing some examples in the [AngularJ](http://www.amazon.com/AngularJS-Brad-Green/dp/1449344852) book from O'Reilly media. I haven't gotten too far yet and I'm already finding lots of typos and it's also a little out of date.

After trying to figure out why I kept getting `$routeProvider: undefined`, a little research showed `ngRoute` is now in `angular-route.js`.

Instead of
{% highlight javascript %}
var aMailServices = angular.module('AMail', []);
{% endhighlight %}

Should be
{% highlight javascript %}
var aMailServices = angular.module('AMail', ['ngRoute']);
{% endhighlight %}

index.html should include
{% highlight html %}
          <script src="lib/angular/angular.js"></script> 
          <script src='lib/angular/angular-route.js'></script>
          <script src="js/controllers.js"></script>
{% endhighlight %}

The book's [errata](http://www.oreilly.com/catalog/errata.csp?isbn=0636920028055) just shows I'll be encountering more.

Happy coding!
