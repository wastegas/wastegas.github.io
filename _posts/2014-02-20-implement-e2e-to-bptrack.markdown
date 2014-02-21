---
layout: post
title: "Implement E2E testing to bptrack app"
date: 2014-02-20 21:23:34
categories: e2e angular-scenario testing
---

Got a simple [E2E (end to end) testing](http://docs.angularjs.org/guide/dev_guide.e2e-testing) implemented on my little project. I'm still trying to wrap my head around how this works. For now, I'm just counting what the repeater is returning for the `tr` element. I'm trying to figure out how to just count the actual records are in the mock data but it's also counting the rows for the header.

To use E2E, you'll need to add it to your project by installing it with [Bower](http://bower.io) by running:

`bower install angular-scenario`

Created files to actually run the test:

public/tests/scenario.js
{% highlight javascript lineos %}
'use strict';

describe('BP list', function() {
    beforeEach(function() {
        browser().navigateTo('/');
        sleep(1);
    });

    it('should list the bp records', function() {
        expect(repeater('tr').count()).toEqual(3);
    })
});
{% endhighlight %}

public/tests/runner.html
{% highlight html lines %}
<!doctype html>
<html lang='en'>
    <head>
        <title>End 2 end test runner</title>
        <script src='/javascripts/vendor/angular-scenario/angular-scenario.js' ng-autotest></script>
        <script src='scenario.js'></script>
    </head>
    <body>
    </body>
</html>
{% endhighlight %}

Happy coding!
