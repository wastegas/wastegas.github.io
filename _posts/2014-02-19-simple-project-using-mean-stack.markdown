---
layout: post
title: "Simple blood pressure tracker using MEAN stack"
date: 2014-02-19 20:44:43
categories: mongodb express angularjs nodejs
---

I'm creating a simple blood pressure tracker app using the [MEAN Stack](http://blog.mongodb.org/post/49262866911/the-mean-stack-mongodb-expressjs-angularjs-and) following Valeri Karpov's [Introduction to the MEAN Stack](http://thecodebarbarian.wordpress.com/2013/07/22/introduction-to-the-mean-stack-part-one-setting-up-your-tools/) writeup. The MEAN shell is already created and some mock data has been added so the app can display some initial data. 

Here's the [source](https://github.com/wastegas/bptrack) of the project. I'll be posting updates as I progress in the project.

The app will be tracking blood pressure readings taken in the morning and evenings and the heart rate. The data will be stored in [mongoDB](http://mongodb.org) using the following document structure:

{% highlight json linenos %}
    {
        datetaken: datevalue,
        time: timevalue,
        systolic: systolicvalue,
        diastolic: diastolicvalue,
        pulse: pulsevalue
    }
{% endhighlight %}

Here's the mock data being declared in routes/index.js
{% highlight javascript linenos %}
exports.index = function(req, res){
  res.render('index', {
      title: 'Express',
      pressures : [
        { datetaken : new Date(new Date()),
          timeofday : 'Morning',
          systolic : 133,
          diastolic: 76,
          pulse : 67
        },
        { datetaken : new Date(new Date()),
          timeofday : 'Evening',
          systolic  : 119,
          diastolic : 79,
          pulse : 66
        },
      ]
  });
};
{% endhighlight %}

I wanted to post snippets of views/index.jade but Jekyll is not rendering the liquid curly braces. So here's the [source](https://github.com/wastegas/bptrack/blob/2dade0e72261200136585dafdd0de66abb1715f2/views/index.jade).

Happy coding!
