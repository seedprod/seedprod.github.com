---
title: Using CSS Frameworks with Thematic
author: John Turner
layout: post
permalink: /using-css-frameworks-with-thematic/
categories:
  - Blog
---
Out of the box the WordPress <a href="http://themeshaper.com" target="_blank">Thematic Theme Framework</a> has several bullet proof css layouts. Sometimes though a project requires a different layout or css.?? I recently had a project where I needed to use the <a href="http://developer.yahoo.com/yui/grids/" target="_blank">YUI CSS Framework</a>. I was able to shove all my code in via Thematic hooks without touching Thematic?s source code. Some people might say this is divitis to the max , which is true, but for the project the benefits out weighed the extra weight of the page. Using this method below you can easily add <a href="http://960.gs/" target="_blank">960 Grids</a>, <a href="http://www.blueprintcss.org/" target="_blank">Blueprint</a>, or whatever CSS framework you?d like. First in the your child theme?s style.css import you theme?s css framework like you would the out of the box layout styles.

<pre>/* Reset browser defaults and Grids */ @import url(&#8216;http://yui.yahooapis.com/combo?2.7.0/build/reset-fonts-grids/reset-fonts-grids.css&#8217;); </pre>

Next we start diving into Thematic?s source code to find the hooks and where we need insert code. So as you can see below I start adding code into these hooks on our child theme?s functions.php file. I don?t recommend using my function naming convention , but I got lazy :) . So with my example all I have to do is change the class on line 3 and I can easily change my layout. Depending on which CSS Framework you use and your layout will depend on which hooks you use. Just start going through the source code and figure out how to start wrapping current elements with your css framework. Also you can use the add_action priority and remove action to do anything you want. If you want to use YUI feel free to use the code below. View my source code on this theme to see it in action.?

<script src="https://gist.github.com/272617.js"></script>
