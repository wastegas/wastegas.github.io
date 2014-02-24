---
layout: post
title: 'Add records to Mongodb'
date: 2014-02-23 19:15:45
categories: bptrack angularjs ng-class bootstrap
---

The [bptrack app](https://github.com/wastegas/bptrack) got some significant progress. The app now adds records into MongoDB database. Also added some bootstrap styling to the data table. Still a lot more to do in this area. Made use of angularjs' [ng-class](http://docs.angularjs.org/api/ng/directive/ngClass) in the table row repeater to conditionally change the background color of the table data based on the values of the Stolic and Diastolic data. 

The ng-class is declared as `ng-class=getClass()` in `index.jade`
{% highlight javascript linenos %}
    $scope.getClass = function(pressure) {
        if(pressure.systolic < 120 && pressure.diastolic < 80) {
            return 'success';
        } else if(pressure.systolic >= 140 && pressure.systolic <=159 || pressure.diastolic >= 90 && pressure.diastolic <= 99) {
                return 'stage1';
        } else if(pressure.systolic > 120 && pressure.systolic <= 139 || pressure.diastolic >= 80 && pressure.diastolic <= 89) {
                return 'warning';
        } else {
            return 'danger';
        }
    };
{% endhighlight %}

I'll be updating the E2E testing to handle these changes.

Happy coding!
