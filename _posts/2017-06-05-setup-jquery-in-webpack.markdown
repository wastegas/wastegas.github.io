---
layout: post
title: Setup jquery in webpack
date: 2017-06-04 09:12:00
categories: jquery webpack 
---
As I mentioned in my previous [post](https://wastegas.github.io/jquery/css/javascript/freecodecamp/webpack/bootstrap/2017/06/04/pomodoro-clock/), I found out the way to setup [jquery](https://jquery.com/) in [webpack](https://webpack.js.org/). I decided to share it here and hopefully someone will find this useful.

Install jquery via npm
```
npm i jquery
```

Add the following lines to the `plugins` section of your `webpack.config.js` file.
```json
plugins: [
	new webpack.ProvidePlugin({
		$:'jquery',
		jQuery: 'jquery'
	})
]
```

Start your dev server and test it by opening the browser console and typing `$`. When you hit enter, it should return `function bound ()`.
