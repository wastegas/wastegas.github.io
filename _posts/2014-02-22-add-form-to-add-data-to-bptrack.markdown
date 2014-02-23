---
layout: post
title: 'Add form to add new data to bptrack'
date: 2014-02-22 20:45:33
categories: bptrack angularjs bootstrap-ui form jade datepicker
---

Added a form skeleton to add data later.  Incorporated [UI Bootstrap datepicker](http://angular-ui.github.io/bootstrap/#datepicker) which is pretty cool.

This can be installed via bower:
`bower install angular-bootstrap`

Then adding `ui-bootstrap` as a module dependency.
{% highlight javascript %}
angular.module('PressureModule', ['ui.bootstrap']);
{% endhighlight %}

For the `time` field, angularjs was adding an extra undefined option for the `<select>` element. I found this explanation in [Stackoverflow](http://stackoverflow.com/questions/12654631/why-does-angularjs-include-an-empty-option-in-select) and used [ng-options](http://docs.angularjs.org/api/ng/directive/select) to create the `Morning` and `Evening` options.

Here's the [diff](https://github.com/wastegas/bptrack/commit/8357cc6dd3b18399255b2bb168093718a70d3bfe) for the latest commit.

Happy coding!
