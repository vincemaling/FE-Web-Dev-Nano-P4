Web Optimization Project
==================
#####Udacity FE Web Developer Nanodegree - Project 4#####
---

Contents
--------

1. [How to Run / Test](#chapter-1)  
2. [Optimizations Performed](#chapter-2)  
3. [Resources Used](#chapter-3)    

How to Run / Test <a id="chapter-1"></a>
-----------------
There are two ways for you to test/demo my Web Optimization work:    

1. Simply visit the [live version](http://www.sweetwaterhandball/opt/index.html "Web Optimization Project") hosted on my web server.  
2. Download the Git ZIP, extract, and run maps.html on your favorite browser. 

Each page has optimized to achieve a 90+ Google PageSpeed score. In addition, the views/pizza.html page and its associated Javascript have optimized to achieve a 60+ FPS rendering speed. I have included two versions of each HTML page: a production version and a development version.  
- The production versions include minified CSS and Javascript. They are the .html files (e.g. index.html).
- The development versions include no minification, so that you can more easily read through the code and understand what's happening. They are the _dev.html files (e.g. index_dev.html). 

Optimizations Performed <a id="chapter-2"></a>
----------
<table>
<tr><th>Page</th><th>Optimizations</th><th>New PageSpeed Speed Score (Mobile/Desktop)</th></tr>
<tr><td>index.html, project-2048.html, project-webperf.html</td>
<td>
- Optimized all images<br>  
- Inlined CSS and Javascript<br>  
- Minified CSS and Javascript<br>
- Moved Javascript files to end of mark-up<br>  
- Added "asynch" tag to Google Analytics script<br>
- Delivered web font asynchronously
</td>
<td>96/97</td></tr>
<tr><td>project-mobile.html</td>
<td>
- Optimized all images<br>  
- Inlined CSS and Javascript<br>  
- Minified CSS and Javascript<br>  
- Moved Javascript files to end of mark-up<br>
- Added "asynch" tag to Google Analytics script<br>  
- Delivered web font asynchronously
</td>
<td>94/97</td></tr>
<tr><td>views/pizza.html</td>
<td>
- Optimized all images<br>
- Inlined CSS and Javascript<br>
- Minified CSS and Javascript<br>  
- Moved Javascript files to end of mark-up<br>  
</td>
<td>91/96</td></tr>
<tr><td>views/js/main.js</td>
<td>
- Minimized DOM updates by consolidating innerHTML<br>  
- Prevented superfluous DOM elements from being rendered<br>  
- See comments on lines 346, 414, 435, 474, 505, 519 in JS file  
</td>
<td>Consistent FPS of 60+</td></tr>
</table>

Resources Used <a id="chapter-3"></a>
---------
<dl><dt>[Google Fonts] (http://www.google.com/fonts#UsePlace:use/Collection:Open+Sans)</dt>
<dd>I consulted Google Fonts to find an asynchronous way of loading Open Sans. Fortunately, this is one of the primary methods Google provides for loading their web fonts.</dd>  

<dt>[Treehouse Blog] (http://blog.teamtreehouse.com/increase-your-sites-performance-with-hardware-accelerated-css)</dt>
<dd>This blog provided some interesting insight on how to use the browser's 3D rendering power to improve performance (FPS) on animated images (such as the pizza images in the background of pizza.html). Specifically, using the translateZ(0) CSS property. While this wasn't necessary to achieve the 60 FPS goal, it did help pizza.html to exceed that goal by a considerable margin.</dd>

<dt>[Google PageSpeed] (https://developers.google.com/speed/pagespeed/)</dt>
<dd>In addition top Develop Tools, PageSpeed offered valuable insights into how I could improve my pages' performance.</dd>

<dt>Various Minifiers</dt>
<dd>Especially [Javascript Minifier] (http://javascript-minifier.com/) and [CSS Minifier) (http://cssminifier.com/).</dd>
